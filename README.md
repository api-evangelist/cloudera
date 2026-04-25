# Cloudera (cloudera)

Cloudera is a hybrid data platform company offering the Cloudera Data Platform (CDP) for data engineering, data warehousing, machine learning, streaming, and operational data. The platform exposes multiple REST APIs including the CDP Public Cloud Control Plane API for managing environments, datalakes, data hubs and workloads, the Cloudera Manager API for cluster lifecycle and configuration management, and per-service REST APIs across the runtime (Cruise Control, Streams Replication Manager, HBase REST, YARN Queue Manager, etc.). APIs are JSON, support standard CRUD, and are typically authenticated via API access keys, basic auth, or session cookies.

**APIs.json:** [apis.yml](https://raw.githubusercontent.com/api-evangelist/cloudera/refs/heads/main/apis.yml)

## Scope

- **Type:** Index
- **x-type:** company

## Tags

Big Data, Data Engineering, Data Lakehouse, Data Platform, Data Warehouse, Hadoop, Hybrid Cloud, Machine Learning, Streaming

## APIs

### Cloudera CDP Public Cloud Control Plane API
JSON REST control-plane API for managing CDP environments, datalakes, data hubs, ML workspaces, data warehouses, and data engineering services. Uses signed requests with API access keys; cdpcurl is the official CLI.

- [Documentation](https://docs.cloudera.com/cdp-public-cloud/cloud/api/topics/mc-api-overview.html)
- [cdpcurl](https://github.com/cloudera/cdpcurl)

### Cloudera Manager API
JSON REST API at `/api/v{N}` for managing clusters, services, roles, configurations, hosts, parcels, tags and audits. HTTP basic auth using Cloudera Manager UI credentials.

- [Documentation](https://cloudera.github.io/cm_api/)
- [v19 Reference](https://cloudera.github.io/cm_api/apidocs/v19/)

### Cloudera Cruise Control REST API
Rebalancing Kafka clusters, monitoring partition load, and anomaly checks.

- [Documentation](https://docs.cloudera.com/runtime/7.2.18/cctrl-managing/topics/cctrl-using-rest-api.html)

### Streams Replication Manager Service REST API
Cross-cluster Kafka replication topology, lag, and metrics.

- [Documentation](https://docs.cloudera.com/cdp-private-cloud-base/7.1.9/srm-overview/topics/srm-rest-api-overview.html)

### HBase REST Server
REST front-end to HBase tables for get/put/scan/delete operations, namespace and table management.

- [Documentation](https://docs.cloudera.com/cdp-private-cloud-base/latest/accessing-hbase/topics/hbase-installing-rest-server-using-cm.html)

### YARN Queue Manager API
Manage capacity scheduler queues, ACLs, and resource allocations.

- [Documentation](https://docs.cloudera.com/cdp-private-cloud-base/7.1.9/yarn-reference/topics/yarn-qm-using-api.html)

## Common Properties

- [Website](https://www.cloudera.com/)
- [Documentation](https://docs.cloudera.com/)
- [Support](https://my.cloudera.com/knowledge.html)
- [GitHub](https://github.com/cloudera)
- [JSON-LD](json-ld/cloudera-context.jsonld)
- [Spectral](rules/cloudera-rules.yml)

## Maintainers

- **FN:** Kin Lane
- **Email:** kinlane@gmail.com
