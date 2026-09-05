---
name: cloudera-provision-cdp-environment
description: >-
  Register a cloud credential and provision a Cloudera CDP environment on AWS,
  then wait for it to become AVAILABLE. This is the first thing that must exist
  in a CDP account — no datalake, data hub, warehouse or AI workspace can be
  created until an environment is AVAILABLE.
api: Cloudera CDP Public Cloud Control Plane API
spec: openapi/cloudera-environments-openapi.yml
generated: '2026-09-05'
method: generated
source: >-
  Generated from the harvested Cloudera Swagger definitions. Every operationId
  below was verified present in openapi/cloudera-environments-openapi.yml.
operations:
  - getCredentialPrerequisites
  - createAWSCredential
  - listCredentials
  - createAWSEnvironment
  - describeEnvironment
  - listEnvironments
  - deleteEnvironment
---

# Provision a CDP environment on AWS

## Before you start

- **Base URL**: `https://api.us-west-1.cdp.cloudera.com` (also `api.eu-1` and `api.ap-1`; pick the region the account lives in).
- **Every call is `POST`** with `Content-Type: application/json`, even reads and deletes. The path IS the verb: `/api/v1/environments2/<operationId>`.
- **Every call must be signed.** Send `x-altus-auth` (the signature) and `x-altus-date` (an RFC 1123 timestamp in GMT). Use `cdpv1sign` from `cdpcurl`, or the `cdp` CLI, or the Java SDK — do not hand-roll it. See `authentication/cloudera-authentication.yml`.
- **THERE IS NO SANDBOX.** These operations provision real infrastructure in a real cloud account and start a CCU-hourly meter. See `sandbox/cloudera-sandbox.yml`.
- **THERE IS NO IDEMPOTENCY.** No `Idempotency-Key` is accepted anywhere in this API. If `createAWSEnvironment` times out, DO NOT blind-retry — call `listEnvironments` first and check whether the name already exists. See `conventions/cloudera-conventions.yml`.

## Steps

### 1. Find out what the credential needs

`POST /api/v1/environments2/getCredentialPrerequisites`

One of only three rehearsal-shaped operations in the whole API. It returns the policy document and external ID the cross-account role must carry, so you can validate the cloud side before creating anything.

### 2. Check whether a credential already exists

`POST /api/v1/environments2/listCredentials`

Credentials are reusable across environments. Reuse before creating.

### 3. Create the cloud credential

`POST /api/v1/environments2/createAWSCredential`

Registers the cross-account role Cloudera will assume. Returns a `credentialCrn`. Mutating.

### 4. Create the environment

`POST /api/v1/environments2/createAWSEnvironment`

Requires the credential name or CRN plus network and region details. Cloudera provisions a FreeIPA server automatically as part of this call.

Returns **200 immediately** with the environment in a transitional state. This is not a completed operation — there is no `202`, no `Location` header and no operation-status resource.

### 5. Poll until it settles

`POST /api/v1/environments2/describeEnvironment` with `{"environmentName": "<name>"}`

Poll on an interval and read the status field. Stop when it reaches a terminal state (available, or a failed state). Nothing pushes you a completion event — Cloudera's Notification service delivers to email, in-app and Slack, never to an HTTP callback, so **polling is the only option**.

Back off generously: no rate limit is published and no `RateLimit-*` or `Retry-After` header is returned, so you have no budget signal to work with. See `rate-limits/cloudera-rate-limits.yml`.

### 6. If you need to undo

`POST /api/v1/environments2/deleteEnvironment`

**This cascades.** Deleting an environment removes its datalake and every data hub attached to it. There is no undelete, no grace period, and Cloudera states no recovery window. Confirm with a human before calling it.

## Errors

Every operation declares only `200` and `default`. The `default` body is `{"code": "...", "message": "..."}` — not RFC 9457. The only code confirmed by probe is `AUTHENTICATION_FAILURE` (HTTP 401), which is returned for *any* unauthenticated request including ones to paths that do not exist, so a 401 tells you nothing about whether your URL was right.

Keep the `x-cdp-request-id` header from every response — it is on every reply, it is the only correlation handle, and it is what Cloudera support asks for.

See `errors/cloudera-problem-types.yml`.
