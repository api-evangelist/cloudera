---
name: cloudera-machine-user-access-keys
description: >-
  Create a Cloudera CDP machine user, issue it an API access key pair, grant it
  a role, and revoke all of it cleanly — the correct way to give an automated
  agent its own credentials instead of borrowing a human's.
api: Cloudera CDP Public Cloud Control Plane API
spec: openapi/cloudera-iam-openapi.yml
generated: '2026-09-05'
method: generated
source: >-
  Generated from the harvested Cloudera Swagger definitions. Every operationId
  below was verified present in openapi/cloudera-iam-openapi.yml.
operations:
  - listMachineUsers
  - createMachineUser
  - createMachineUserAccessKey
  - listRoles
  - assignMachineUserRole
  - unassignMachineUserRole
  - deleteAccessKey
  - deleteMachineUser
---

# Give an agent its own CDP credentials

## Why a machine user

CDP has no OAuth and no scopes. A caller is authenticated by a signed request and authorised by the IAM role assignments attached to the *actor* behind the key. A machine user is a first-class actor, so it can be granted a narrow role and revoked independently — which a human's personal access key cannot.

> **Path note.** The published IAM definition uses paths of the form `/iam/<operationId>`, without the `/api/v1` prefix every other service definition carries. Cloudera's own `cdpcli` service data does the same and the CLI supplies the prefix. On the wire the documented form is `/api/v1/iam/<operationId>`; a client generated straight from the IAM definition will need the prefix added.

## Steps

### 1. Check for an existing machine user

`POST /api/v1/iam/listMachineUsers`

Names are unique. Creating one that exists fails rather than duplicating — which is the only thing standing in for idempotency on this API.

### 2. Create it

`POST /api/v1/iam/createMachineUser`

### 3. Issue the key pair

`POST /api/v1/iam/createMachineUserAccessKey`

Returns an **access key ID and a private key**. The private key is shown once. Store it in a secret manager immediately — there is no re-read operation.

Never write the private key to a log, a repository, a config file in the working tree, or a message. This is the credential that signs every request.

### 4. Grant least privilege

`POST /api/v1/iam/listRoles` to see what exists, then
`POST /api/v1/iam/assignMachineUserRole` to grant.

For a resource-scoped grant use `assignMachineUserResourceRole` instead, which binds the role to a specific resource CRN rather than the whole account. Prefer it.

Start with read-only roles. 414 of the 778 operations in this API are marked mutating, most of them provision billed infrastructure, and none of them can be replayed safely.

### 5. Revoke

Reversal is complete and immediate at every step:

| Granted | Revoke with |
|---|---|
| Role | `POST /api/v1/iam/unassignMachineUserRole` |
| Resource role | `POST /api/v1/iam/unassignMachineUserResourceRole` |
| Access key | `POST /api/v1/iam/deleteAccessKey` |
| The actor itself | `POST /api/v1/iam/deleteMachineUser` |

Role assignment is the one part of this API where reversal has no time limit — it is pure state, and unassigning restores the prior condition exactly.

## Federated alternatives

If the account already runs a corporate IdP, Cloudera supports both **SAML 2.0** (`createSamlProvider`, `setSamlAuthnRequestSigningKey`, `setSamlResponseDecryptionKey`) and **SCIM** provisioning (`createScimAccessToken`, `listScimAccessTokens`, `deleteScimAccessToken`). SCIM is not available on the Cloudera for Government form factor. See `conformance/cloudera-conformance.yml`.
