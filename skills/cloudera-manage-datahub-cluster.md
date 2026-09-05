---
name: cloudera-manage-datahub-cluster
description: >-
  Create, inspect, scale, stop, start and delete a Cloudera Data Hub workload
  cluster inside an existing CDP environment — including which of those actions
  can be taken back and which cannot.
api: Cloudera CDP Public Cloud Control Plane API
spec: openapi/cloudera-datahub-openapi.yml
generated: '2026-09-05'
method: generated
source: >-
  Generated from the harvested Cloudera Swagger definitions. Every operationId
  below was verified present in openapi/cloudera-datahub-openapi.yml.
operations:
  - listClusterTemplates
  - createAWSCluster
  - describeCluster
  - listClusters
  - scaleCluster
  - stopCluster
  - startCluster
  - deleteCluster
---

# Manage a Data Hub cluster

## Preconditions

An **AVAILABLE environment with a datalake** must already exist — see `cloudera-provision-cdp-environment`. A Data Hub cluster attaches to the environment's datalake for its metadata, security and governance context.

Base URL, POST-only convention and request signing are as in the environment skill.

> **Watch the service prefix.** `describeCluster`, `listClusters` and `deleteCluster` exist in BOTH the Data Hub service and the Data Warehouse service with the same operationId. Always address them by full path — `/api/v1/datahub/describeCluster`, not by operationId alone — or you will drive the wrong product.

## Steps

### 1. Pick a shape

`POST /api/v1/datahub/listClusterTemplates`

Data Hub clusters are built from templates and cluster definitions rather than assembled field by field. List what the account has before authoring anything.

### 2. Create the cluster

`POST /api/v1/datahub/createAWSCluster`

Takes the environment name, the cluster name and the template or definition. Returns 200 immediately with the cluster in a transitional state; the cluster is not usable yet.

Cost starts here: Data Hub meters at $0.04/CCU-hour (see `plans/cloudera-plans-pricing.yml`).

### 3. Poll to ready

`POST /api/v1/datahub/describeCluster`

Poll and read the status until it reaches a terminal state.

### 4. Change size

`POST /api/v1/datahub/scaleCluster`

Mutating. There is no dry-run for this — the API has no general rehearse mode.

### 5. Choose the right way to stop

Two very different actions:

| Action | Path | Reversible? |
|---|---|---|
| Stop | `/api/v1/datahub/stopCluster` | **Yes** — `startCluster` brings it back |
| Delete | `/api/v1/datahub/deleteCluster` | **No** — permanent, no stated recovery window |

**Prefer `stopCluster` whenever the intent is "stop paying for this".** It halts the meter and keeps the cluster recoverable. `deleteCluster` is unrecoverable and Cloudera publishes no grace period. If an instruction is ambiguous between the two, stop, and ask.

### 6. Restart

`POST /api/v1/datahub/startCluster`

## Retry rule

No idempotency mechanism exists anywhere in this API. If `createAWSCluster` or `scaleCluster` times out, call `listClusters` and reconcile before retrying. A blind retry can produce a second cluster and a second meter.
