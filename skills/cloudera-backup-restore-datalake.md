---
name: cloudera-backup-restore-datalake
description: >-
  Back up a Cloudera datalake, check the backup, restore from it, and cancel a
  running backup or restore. The reversal path for the most consequential state
  in a CDP account.
api: Cloudera CDP Public Cloud Control Plane API
spec: openapi/cloudera-datalake-openapi.yml
generated: '2026-09-05'
method: generated
source: >-
  Generated from the harvested Cloudera Swagger definitions. Every operationId
  below was verified present in openapi/cloudera-datalake-openapi.yml.
operations:
  - listDatalakes
  - describeDatalake
  - backupDatalake
  - listDatalakeBackups
  - restoreDatalake
  - restoreDatalakeStatus
  - cancelBackup
  - cancelRestore
  - deleteDatalake
---

# Back up and restore a datalake

The datalake holds the environment's shared metadata, security policies and governance catalogue. Losing it loses the meaning of everything stored under the environment, which is why this is the one place in the CDP API where the reversal path is first-class.

## Steps

### 1. Locate the datalake

`POST /api/v1/datalake/listDatalakes`, then `POST /api/v1/datalake/describeDatalake`

There is exactly one datalake per environment. Confirm its status is terminal-healthy before starting a backup.

### 2. Take a backup

`POST /api/v1/datalake/backupDatalake`

Mutating and long-running. Returns 200 immediately.

### 3. Track it

`POST /api/v1/datalake/listDatalakeBackups`

Poll until the backup you started reports complete.

### 4. Abandon a run if you need to

`POST /api/v1/datalake/cancelBackup` or `POST /api/v1/datalake/cancelRestore`

Both exist and both are safe to call on a run that is still in flight.

### 5. Restore

`POST /api/v1/datalake/restoreDatalake`, then poll `POST /api/v1/datalake/restoreDatalakeStatus`

## What Cloudera does NOT tell you

**Retention is undocumented.** Cloudera publishes no statement of how long a datalake backup is kept, and no restore window. `restoreDatalake` exists, but nothing in the contract or the API documentation says a backup taken today will still be restorable on any given future date.

**Do not assert a window to a user.** If asked "how long do I have to restore this", the honest answer is that Cloudera does not publish one and it must be confirmed with Cloudera support or read from the account's own configuration. Inventing a number here is the one mistake in this skill that could cost real data.

See `conventions/cloudera-conventions.yml` → `reversibility`, which grades Cloudera as `documented` rather than `verified` for exactly this reason: the reversal operations exist; the clock does not.

### 6. Deletion is separate and final

`POST /api/v1/datalake/deleteDatalake` is not part of a backup workflow. It is permanent, and `deleteEnvironment` triggers it implicitly. Take a backup first, always.
