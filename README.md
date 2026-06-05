# Cloudera (cloudera)

Cloudera is a hybrid data platform company offering the Cloudera Data Platform (CDP) for data engineering, data warehousing, machine learning, streaming, and operational data. The platform exposes multiple REST APIs including the CDP Public Cloud Control Plane API for managing environments, datalakes, data hubs and workloads, the Cloudera Manager API for cluster lifecycle and configuration management, and per-service REST APIs across the runtime (Cruise Control, Streams Replication Manager, HBase REST, YARN Queue Manager, etc.). APIs are JSON, support standard CRUD, and are typically authenticated via API access keys, basic auth, or session cookies.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/cloudera/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/cloudera/refs/heads/main/apis.yml)

## Scope

- **Type:** Index

## Tags

- Big Data
- Data Engineering
- Data Lakehouse
- Data Platform
- Data Warehouse
- Hadoop
- Hybrid Cloud
- Machine Learning
- Streaming

## Timestamps

- **Created:** 2024-01-01
- **Modified:** 2026-04-25

## APIs

### Cloudera CDP Public Cloud Control Plane API

The Cloudera CDP Public Cloud Control Plane REST API manages CDP environments, datalakes, data hubs, machine learning workspaces, data warehouses and data engineering services. Access requires a Cloudera user account with an API access key and private key. cdpcurl is the Python CLI for signed calls.

- **Human URL:** [https://docs.cloudera.com/cdp-public-cloud/cloud/api/topics/mc-api-overview.html](https://docs.cloudera.com/cdp-public-cloud/cloud/api/topics/mc-api-overview.html)

#### Tags

- Cloud
- Control Plane
- CDP
- Environments

#### Properties

- [Documentation](https://docs.cloudera.com/cdp-public-cloud/cloud/api/topics/mc-api-overview.html)
- [C L I](https://github.com/cloudera/cdpcurl)
- [Postman Collection](collections/cloudera.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cloudera.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Cloudera Manager API

Cloudera Manager exposes a JSON REST API at /api/v{N} for managing clusters, services, roles, configurations, hosts, parcels, tags and audits. Authentication uses HTTP basic auth with the same credentials as the Cloudera Manager web UI; subsequent requests can use the session cookie returned on authentication.

- **Human URL:** [https://cloudera.github.io/cm_api/](https://cloudera.github.io/cm_api/)

#### Tags

- Cluster
- Configuration
- Management

#### Properties

- [Documentation](https://cloudera.github.io/cm_api/)
- [Reference](https://cloudera.github.io/cm_api/apidocs/v19/)
- [Overview](https://docs.cloudera.com/cdp-private-cloud-base/7.1.9/concepts/topics/cm-api-overview.html)
- [Postman Collection](collections/cloudera.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cloudera.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Cloudera Cruise Control REST API

Cruise Control on CDP exposes REST endpoints for rebalancing Kafka clusters, monitoring partition load, and triggering anomaly checks.

- **Human URL:** [https://docs.cloudera.com/runtime/7.2.18/cctrl-managing/topics/cctrl-using-rest-api.html](https://docs.cloudera.com/runtime/7.2.18/cctrl-managing/topics/cctrl-using-rest-api.html)

#### Tags

- Kafka
- Rebalancing
- Streaming

#### Properties

- [Documentation](https://docs.cloudera.com/runtime/7.2.18/cctrl-managing/topics/cctrl-using-rest-api.html)
- [Postman Collection](collections/cloudera.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cloudera.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Streams Replication Manager Service REST API

Streams Replication Manager (SRM) exposes a REST API for inspecting cross-cluster Kafka replication topology, lag, and metrics.

- **Human URL:** [https://docs.cloudera.com/cdp-private-cloud-base/7.1.9/srm-overview/topics/srm-rest-api-overview.html](https://docs.cloudera.com/cdp-private-cloud-base/7.1.9/srm-overview/topics/srm-rest-api-overview.html)

#### Tags

- Kafka
- Replication
- Streaming

#### Properties

- [Documentation](https://docs.cloudera.com/cdp-private-cloud-base/7.1.9/srm-overview/topics/srm-rest-api-overview.html)
- [Postman Collection](collections/cloudera.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cloudera.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### HBase REST Server

The HBase REST Server provides a REST front-end to HBase tables for get/put/scan/delete, namespace and table management - installable via Cloudera Manager.

- **Human URL:** [https://docs.cloudera.com/cdp-private-cloud-base/latest/accessing-hbase/topics/hbase-installing-rest-server-using-cm.html](https://docs.cloudera.com/cdp-private-cloud-base/latest/accessing-hbase/topics/hbase-installing-rest-server-using-cm.html)

#### Tags

- HBase
- NoSQL
- REST

#### Properties

- [Documentation](https://docs.cloudera.com/cdp-private-cloud-base/latest/accessing-hbase/topics/hbase-installing-rest-server-using-cm.html)
- [Postman Collection](collections/cloudera.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cloudera.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### YARN Queue Manager API

YARN Queue Manager exposes a REST API for managing capacity scheduler queues, ACLs, and resource allocations on a CDP cluster.

- **Human URL:** [https://docs.cloudera.com/cdp-private-cloud-base/7.1.9/yarn-reference/topics/yarn-qm-using-api.html](https://docs.cloudera.com/cdp-private-cloud-base/7.1.9/yarn-reference/topics/yarn-qm-using-api.html)

#### Tags

- YARN
- Resource Management
- Scheduling

#### Properties

- [Documentation](https://docs.cloudera.com/cdp-private-cloud-base/7.1.9/yarn-reference/topics/yarn-qm-using-api.html)
- [Postman Collection](collections/cloudera.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cloudera.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [LinkedIn](https://www.linkedin.com/company/cloudera)
- [Website](https://www.cloudera.com/)
- [Documentation](https://docs.cloudera.com/)
- [Support](https://my.cloudera.com/knowledge.html)
- [Privacy Policy](https://www.cloudera.com/legal/privacy.html)
- [Git Hub](https://github.com/cloudera)
- [JSON-LD](json-ld/cloudera-context.jsonld) — [JSON-LD](https://www.w3.org/TR/json-ld11/)
- [Spectral Rules](rules/cloudera-rules.yml) — [Spectral](https://docs.stoplight.io/docs/spectral)

## Maintainers

**FN:** Kin Lane
**Email:** kinlane@gmail.com
