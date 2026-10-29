# Cloudera

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Cloudera is a hybrid data platform company offering the Cloudera Data Platform (CDP) for data engineering, data warehousing, machine learning, streaming, and operational data. The platform exposes multiple REST APIs including the CDP Public Cloud Control Plane API for managing environments, datalakes, data hubs and workloads, the Cloudera Manager API for cluster lifecycle and configuration management, and per-service REST APIs across the runtime (Cruise Control, Streams Replication Manager, HBase REST, YARN Queue Manager, etc.). APIs are JSON, support standard CRUD, and are typically authenticated via API access keys, basic auth, or session cookies.

**Areas:** Big Data · Data Engineering · Data Lakehouse · Data Platform · Data Warehouse · Hadoop · Hybrid Cloud · Machine Learning · Streaming

## Cloudera on APIs.io

Everything profiled for Cloudera is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/cloudera/](https://apis.io/providers/cloudera/)** — or go straight to one of the APIs or properties below.

### APIs (24)

- [Cloudera Manager API](https://apis.io/apis/cloudera/manager/) — Cloudera Manager exposes a JSON REST API at /api/v{N} for managing clusters, services, roles, configurations, hosts, parcels, tags and audits.…
- [Cloudera Cruise Control REST API](https://apis.io/apis/cloudera/cruise-control/) — Cruise Control on CDP exposes REST endpoints for rebalancing Kafka clusters, monitoring partition load, and triggering anomaly checks.
- [Streams Replication Manager Service REST API](https://apis.io/apis/cloudera/srm/) — Streams Replication Manager (SRM) exposes a REST API for inspecting cross-cluster Kafka replication topology, lag, and metrics.
- [HBase REST Server](https://apis.io/apis/cloudera/hbase-rest/) — The HBase REST Server provides a REST front-end to HBase tables for get/put/scan/delete, namespace and table management - installable via Cloudera Manager.
- [YARN Queue Manager API](https://apis.io/apis/cloudera/yarn-queue-manager/) — YARN Queue Manager exposes a REST API for managing capacity scheduler queues, ACLs, and resource allocations on a CDP cluster.
- [Cloudera Audit API](https://apis.io/apis/cloudera/cloudera-audit-api/) — The Audit API from Cloudera — 11 operation(s) for audit.
- [Cloudera CDF Local RPCAPI Version1 API](https://apis.io/apis/cloudera/cloudera-cdflocalrpcapiversion1-api/) — The CDFLocalRPCAPIVersion1 API from Cloudera — 71 operation(s) for cdflocalrpcapiversion1.
- [Cloudera Cloudprivatelinks API](https://apis.io/apis/cloudera/cloudera-cloudprivatelinks-api/) — The Cloudprivatelinks API from Cloudera — 9 operation(s) for cloudprivatelinks.
- [Cloudera Compute API](https://apis.io/apis/cloudera/cloudera-compute-api/) — The Compute API from Cloudera — 15 operation(s) for compute.
- [Cloudera Consumption API](https://apis.io/apis/cloudera/cloudera-consumption-api/) — The Consumption API from Cloudera — 1 operation(s) for consumption.
- [Cloudera Datalake API](https://apis.io/apis/cloudera/cloudera-datalake-api/) — The Datalake API from Cloudera — 56 operation(s) for datalake.
- [Cloudera De API](https://apis.io/apis/cloudera/cloudera-de-api/) — The De API from Cloudera — 24 operation(s) for de.
- [Cloudera Df API](https://apis.io/apis/cloudera/cloudera-df-api/) — The Df API from Cloudera — 66 operation(s) for df.
- [Cloudera Drscp API](https://apis.io/apis/cloudera/cloudera-drscp-api/) — The Drscp API from Cloudera — 9 operation(s) for drscp.
- [Cloudera Dw API](https://apis.io/apis/cloudera/cloudera-dw-api/) — The Dw API from Cloudera — 95 operation(s) for dw.
- [Cloudera Environments2 API](https://apis.io/apis/cloudera/cloudera-environments2-api/) — The Environments2 API from Cloudera — 104 operation(s) for environments2.
- [Cloudera Iam API](https://apis.io/apis/cloudera/cloudera-iam-api/) — The Iam API from Cloudera — 79 operation(s) for iam.
- [Cloudera Imagecatalog API](https://apis.io/apis/cloudera/cloudera-imagecatalog-api/) — The Imagecatalog API from Cloudera — 11 operation(s) for imagecatalog.
- [Cloudera Lakehouseopt API](https://apis.io/apis/cloudera/cloudera-lakehouseopt-api/) — The Lakehouseopt API from Cloudera — 30 operation(s) for lakehouseopt.
- [Cloudera Ml API](https://apis.io/apis/cloudera/cloudera-ml-api/) — The Ml API from Cloudera — 59 operation(s) for ml.
- [Cloudera Opdb API](https://apis.io/apis/cloudera/cloudera-opdb-api/) — The Opdb API from Cloudera — 19 operation(s) for opdb.
- [Cloudera Replicationmanager API](https://apis.io/apis/cloudera/cloudera-replicationmanager-api/) — The Replicationmanager API from Cloudera — 24 operation(s) for replicationmanager.
- [Cloudera Data Catalog API](https://apis.io/apis/cloudera/cloudera-data-catalog-api/) — The Data Catalog API from Cloudera — 20 operation(s) for data catalog.
- [Cloudera Data Hub API](https://apis.io/apis/cloudera/cloudera-data-hub-api/) — The Data Hub API from Cloudera — 75 operation(s) for data hub.

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### MCP servers (1)

Model Context Protocol servers that expose the API to agents.

- [cloudera-mcp.yml](https://apis.io/servers/cloudera/cloudera-mcp-yml/)

#### Agentic access (1)

Which operations an agent can call, which act, and which need a human in the loop.

- [Cloudera Agentic Access](https://apis.io/agentic-access/cloudera/cloudera-agentic-access/)

#### JSON Schema (101)

The data models the API reads and writes.

- [AddFlowToDeploymentRequest](https://apis.io/schemas/cloudera/cloudera-add-flow-to-deployment-request/)
- [ArchiveAuditEventsResponse](https://apis.io/schemas/cloudera/cloudera-archive-audit-events-response/)
- [AuthorizePrivateLinkServiceAccessRequest](https://apis.io/schemas/cloudera/cloudera-authorize-private-link-service-access-request/)
- [ChangeFlowVersionInDeploymentRequest](https://apis.io/schemas/cloudera/cloudera-change-flow-version-in-deployment-request/)
- [ChangeFlowVersionRequest](https://apis.io/schemas/cloudera/cloudera-change-flow-version-request/)
- [ChangeTablePolicyRequest](https://apis.io/schemas/cloudera/cloudera-change-table-policy-request/)
- [CollectCmDiagnosticsRequest](https://apis.io/schemas/cloudera/cloudera-collect-cm-diagnostics-request/)
- [CollectDatahubDiagnosticsRequest](https://apis.io/schemas/cloudera/cloudera-collect-datahub-diagnostics-request/)
- [CollectDatalakeDiagnosticsRequest](https://apis.io/schemas/cloudera/cloudera-collect-datalake-diagnostics-request/)
- [CollectDiagnosticBundleResponse](https://apis.io/schemas/cloudera/cloudera-collect-diagnostic-bundle-response/)
- [CollectDiagnosticsRequest](https://apis.io/schemas/cloudera/cloudera-collect-diagnostics-request/)
- [CollectFreeipaDiagnosticsRequest](https://apis.io/schemas/cloudera/cloudera-collect-freeipa-diagnostics-request/)
- [ConfigureArchivingRequest](https://apis.io/schemas/cloudera/cloudera-configure-archiving-request/)
- [CreateAbfsCredentialRequest](https://apis.io/schemas/cloudera/cloudera-create-abfs-credential-request/)
- [CreateAwsClusterRequest](https://apis.io/schemas/cloudera/cloudera-create-aws-cluster-request/)
- [CreateAwsCredentialRequest](https://apis.io/schemas/cloudera/cloudera-create-aws-credential-request/)
- [CreateAWSClusterRequest](https://apis.io/schemas/cloudera/cloudera-create-awscluster-request/)
- [CreateAWSDatalakeRequest](https://apis.io/schemas/cloudera/cloudera-create-awsdatalake-request/)
- [CreateAWSEnvironmentRequest](https://apis.io/schemas/cloudera/cloudera-create-awsenvironment-request/)
- [CreateAWSGovCloudClusterRequest](https://apis.io/schemas/cloudera/cloudera-create-awsgov-cloud-cluster-request/)
- [CreateAWSGovCloudDatalakeRequest](https://apis.io/schemas/cloudera/cloudera-create-awsgov-cloud-datalake-request/)
- [CreateAWSGovCloudEnvironmentRequest](https://apis.io/schemas/cloudera/cloudera-create-awsgov-cloud-environment-request/)
- [CreateAzureClusterRequest](https://apis.io/schemas/cloudera/cloudera-create-azure-cluster-request/)
- [CreateAzureDatalakeRequest](https://apis.io/schemas/cloudera/cloudera-create-azure-datalake-request/)
- [CreateAzureEnvironmentRequest](https://apis.io/schemas/cloudera/cloudera-create-azure-environment-request/)
- …and 76 more published on APIs.io

#### JSON-LD (1)

Linked-data contexts for the provider's vocabulary.

- [Cloudera Context](https://apis.io/jsonld/cloudera/cloudera-context/)

#### Collections (7)

Postman and Open Collection request collections.

- [Moved to /providers/cloudera/](https://apis.io/collections/cloudera/open-cloudera/)
- [Moved to /providers/cloudera/](https://apis.io/collections/cloudera/open-cloudera-dataengineering-api/)
- [Moved to /providers/cloudera/](https://apis.io/collections/cloudera/open-cloudera-datahub-api/)
- [Moved to /providers/cloudera/](https://apis.io/collections/cloudera/open-cloudera-datalake-api/)
- [Moved to /providers/cloudera/](https://apis.io/collections/cloudera/open-cloudera-environments-api/)
- [Moved to /providers/cloudera/](https://apis.io/collections/cloudera/open-cloudera-iam-api/)
- [Moved to /providers/cloudera/](https://apis.io/collections/cloudera/open-cloudera-ml-api/)

#### Overlays (38)

OpenAPI overlays, including conversational phrasing for each operation.

- [Cloudera Audit Api Phrasing Overlay](https://apis.io/overlays/cloudera/cloudera-audit-api-phrasing-overlay/)
- [Cloudera Audit Overlay](https://apis.io/overlays/cloudera/cloudera-audit-overlay/)
- [Cloudera Cdflocalrpcapiversion1 Api Phrasing Overlay](https://apis.io/overlays/cloudera/cloudera-cdflocalrpcapiversion1-api-phrasing-overlay/)
- [Cloudera Cloudprivatelinks Api Phrasing Overlay](https://apis.io/overlays/cloudera/cloudera-cloudprivatelinks-api-phrasing-overlay/)
- [Cloudera Cloudprivatelinks Overlay](https://apis.io/overlays/cloudera/cloudera-cloudprivatelinks-overlay/)
- [Cloudera Compute Api Phrasing Overlay](https://apis.io/overlays/cloudera/cloudera-compute-api-phrasing-overlay/)
- [Cloudera Compute Overlay](https://apis.io/overlays/cloudera/cloudera-compute-overlay/)
- [Cloudera Consumption Api Phrasing Overlay](https://apis.io/overlays/cloudera/cloudera-consumption-api-phrasing-overlay/)
- [Cloudera Consumption Overlay](https://apis.io/overlays/cloudera/cloudera-consumption-overlay/)
- [Cloudera Data Catalog Api Phrasing Overlay](https://apis.io/overlays/cloudera/cloudera-data-catalog-api-phrasing-overlay/)
- [Cloudera Data Hub Api Phrasing Overlay](https://apis.io/overlays/cloudera/cloudera-data-hub-api-phrasing-overlay/)
- [Cloudera Datacatalog Overlay](https://apis.io/overlays/cloudera/cloudera-datacatalog-overlay/)
- [Cloudera Datahub Overlay](https://apis.io/overlays/cloudera/cloudera-datahub-overlay/)
- [Cloudera Datalake Api Phrasing Overlay](https://apis.io/overlays/cloudera/cloudera-datalake-api-phrasing-overlay/)
- [Cloudera Datalake Overlay](https://apis.io/overlays/cloudera/cloudera-datalake-overlay/)
- [Cloudera De Api Phrasing Overlay](https://apis.io/overlays/cloudera/cloudera-de-api-phrasing-overlay/)
- [Cloudera De Overlay](https://apis.io/overlays/cloudera/cloudera-de-overlay/)
- [Cloudera Df Api Phrasing Overlay](https://apis.io/overlays/cloudera/cloudera-df-api-phrasing-overlay/)
- [Cloudera Df Overlay](https://apis.io/overlays/cloudera/cloudera-df-overlay/)
- [Cloudera Dfworkload Overlay](https://apis.io/overlays/cloudera/cloudera-dfworkload-overlay/)
- [Cloudera Drscp Api Phrasing Overlay](https://apis.io/overlays/cloudera/cloudera-drscp-api-phrasing-overlay/)
- [Cloudera Drscp Overlay](https://apis.io/overlays/cloudera/cloudera-drscp-overlay/)
- [Cloudera Dw Api Phrasing Overlay](https://apis.io/overlays/cloudera/cloudera-dw-api-phrasing-overlay/)
- [Cloudera Dw Overlay](https://apis.io/overlays/cloudera/cloudera-dw-overlay/)
- [Cloudera Environments Overlay](https://apis.io/overlays/cloudera/cloudera-environments-overlay/)
- …and 13 more published on APIs.io

#### Governance rules (1)

Spectral rulesets for the provider's contracts.

- [Cloudera API Rules](https://apis.io/rules/cloudera/cloudera-rules/)

#### Security (3)

Authentication, trust centre, and vulnerability disclosure.

- [Cloudera Authentication](https://apis.io/security/cloudera/cloudera-authentication/)
- [Cloudera Domain Security](https://apis.io/security/cloudera/cloudera-domain-security/)
- [Cloudera Trust Center](https://apis.io/security/cloudera/cloudera-trust-center/)

#### Plans and pricing (1)

Published plans, tiers and prices.

- [Cloudera Plans Pricing](https://apis.io/plans/cloudera/cloudera-plans-pricing/)

#### Rate limits (1)

Published request limits.

- [Cloudera Rate Limits](https://apis.io/rate-limits/cloudera/cloudera-rate-limits/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://www.cloudera.com/)
- [Documentation](https://docs.cloudera.com/)
- [Getting started](https://docs.cloudera.com/cdp-public-cloud/cloud/index.html)
- [API reference](https://cloudera.github.io/cdp-dev-docs/api-docs/)
- [Pricing](https://www.cloudera.com/products/pricing.html)
- [Sign up](https://www.cloudera.com/campaign/try-cdp-public-cloud.html)
- [Support](https://community.cloudera.com/)
- [Blog](https://www.cloudera.com/blog.html)
- [Terms of service](https://www.cloudera.com/legal/terms-and-conditions.html)
- [Privacy policy](https://www.cloudera.com/legal/policies.html)
- [GitHub](https://github.com/cloudera)
- [Status](https://status.cloudera.com/)

## API Evangelist rating

**Kin Score 66.8** — exemplar · rubric 0.25.0 · scored 2026-10-23

| Facet | Score |
|---|---|
| Discoverability | 70.0 |
| Contract quality | 45.5 |
| Contract governance | 19.7 |
| Operational transparency | 42.1 |
| Developer ergonomics | 80.4 |
| Access clarity | 92.1 |

**Agent readiness 28.9** — agent-ready

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | derived (partial credit) |
| Reversibility Documented | documented (partial credit) |
| MCP Server | documented (partial credit) |
| Auth Clarity | bearer (partial credit) |
| Idempotency | derived (partial credit) |
| Error Semantics | derived (partial credit) |
| OpenAPI Examples | — |
| Rate Limit Signal | documented (partial credit) |
| Event Surface Described | — |
| Agent Skills | derived (partial credit) |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | — |
| Protected Resource Metadata | — |
| Dynamic Client Registration | — |
| Agentic Commerce | — |
| Pagination Ratio | na |
| Operation Distinctiveness | distinct |

**Regulatory alignment 27.3** — Horizontal (data, software, accessibility, platform)

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/cloudera/](https://apis.io/providers/cloudera/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for Cloudera: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/cloudera/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
