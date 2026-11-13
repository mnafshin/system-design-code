# System Design companion code

Companion code for the planned **System Design / Architecture** YouTube channel (public channel name TBD).

Planning only: there is no code in this repository yet. Folders will be added when a topic is produced. Each topic gets one folder, tagged or linked from the matching video.

- Private channel working repo: [mnafshin/system-design-channel](https://github.com/mnafshin/system-design-channel)
- Curriculum (source of truth): [docs/CURRICULUM.md](https://github.com/mnafshin/system-design-channel/blob/main/docs/CURRICULUM.md)
- Articles (planned section, not live until the site PR is merged): [mnafshin.info/system-design](https://mnafshin.info/system-design/)

The running example is Securities Order Intake on a shared internal platform used by 40+ teams. This repo is for architecture-level examples. Spring implementations stay on [springuniverse-code](https://github.com/mnafshin/springuniverse-code). Whether older public repos ([idempotency](https://github.com/mnafshin/idempotency), [multi-tenancy](https://github.com/mnafshin/multi-tenancy), [locks-in-java](https://github.com/mnafshin/locks-in-java)) are folded in is still open.

## Planned layout

One folder per curriculum topic, in learning order A → B → C.

### Part A — Communication and events

| Folder | Topic |
|---|---|
| `SD01-sync-vs-async/` | Sync vs async; when events beat calls |
| `SD02-protocol-selection/` | Protocol selection: REST vs gRPC for internal calls, protobuf conventions, gRPC-JSON transcoding at the edge, event bridge |
| `SD03-queues-vs-logs/` | Queues vs logs: SNS/SQS vs Kafka |
| `SD04-dual-write/` | Publishing after commit and the dual-write problem |
| `SD05-transactional-outbox/` | Transactional outbox and relay |
| `SD06-delivery-guarantees/` | Delivery guarantees: at-least-once, ordering, partitions |
| `SD07-idempotency/` | Idempotency end to end: Idempotency-Key APIs and idempotent consumers |
| `SD08-retries-dlq-replay/` | Retries, DLQ and replay |
| `SD09-event-schemas/` | Event schemas: Avro, schema registry, compatibility modes (BACKWARD default), safe evolution, contract tests |
| `SD10-sagas/` | Sagas and long-running workflows |

### Part B — Data integration and reliability

| Folder | Topic |
|---|---|
| `SD11-cdc-and-consistency/` | Change data capture (Debezium/Kafka Connect), bulk migration and backfill, acquisitions/ETL as architecture; eventual consistency trade-offs |
| `SD12-concurrency-control/` | Concurrency control across services: optimistic vs distributed locks |
| `SD13-resilience/` | Resilience: timeouts, retries, circuit breakers, bulkheads, rate limits |
| `SD14-cqrs-read-models/` | Read models and CQRS (e.g. search index as the read side) |
| `SD15-four-ids-and-tracing/` | The four IDs (tenant, trace, correlation, request) and distributed tracing as a design concern |
| `SD16-observability-cutover/` | Observability migration with a collector and dual-write cutover |

### Part C — Platform governance

| Folder | Topic |
|---|---|
| `SD17-slos-and-error-budgets/` | NFRs, SLOs and error budgets |
| `SD18-adrs-and-rfcs/` | ADRs and RFCs across teams |
| `SD19-platform-vs-product/` | Platform vs product boundaries; what to centralize; avoiding the blocking platform team |
| `SD20-paved-road/` | Paved road vs escape hatch |
| `SD21-developer-portal/` | Developer portal and service catalog: Backstage, scaffolding templates, catalog-first, unique service names |
| `SD22-shared-libraries-and-boms/` | Shared libraries and BOMs: versioning, backward-compatibility support windows, version lifecycle, deprecation, upgrade paths, fleet-wide migration |
| `SD23-rollout-for-many-teams/` | Rollout strategy for 40+ teams: waves, opt-in, success metrics |
| `SD24-polyglot-platforms/` | Polyglot platforms: one convention across JVM, Node and Python |
| `SD25-risk-and-what-not-to-build/` | Risk registers and choosing what NOT to build |
| `SD26-platform-and-business-outcomes/` | Connecting platform strategy to business outcomes |

These folders are not created yet.
