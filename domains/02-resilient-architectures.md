# Domain 2 — Design Resilient Architectures (26%)

> **Outcome:** Design scalable, loosely coupled, highly available, fault-tolerant, and recoverable systems.

## Availability and fault isolation

Distribute critical components across Availability Zones and avoid shared single points of failure. A load balancer routes to healthy targets; Auto Scaling replaces unhealthy capacity and adjusts fleet size. Keep application tiers stateless where practical and externalize session state.

High availability minimizes interruption; fault tolerance aims to continue through faults with little or no disruption. Multi-Region is justified by business requirements such as regional disaster recovery, global latency, or sovereignty—not by default.

## Decoupling patterns

- **SQS:** durable queue for buffering, smoothing spikes, and asynchronous worker processing.
- **SNS:** push-based pub/sub and fan-out to multiple subscribers.
- **EventBridge:** event bus with rule-based routing among producers and targets.
- **Step Functions:** workflow orchestration, state, retries, and branching.

Design consumers to be idempotent because distributed delivery can repeat. Use dead-letter queues for messages that repeatedly fail processing.

## Disaster recovery

| Strategy | Relative recovery | Relative cost |
|---|---|---|
| Backup and restore | Slowest | Lowest |
| Pilot light | Core data/services always ready | Low–medium |
| Warm standby | Scaled-down working environment | Medium–high |
| Multi-site active/active | Fastest | Highest |

**RTO** is the maximum acceptable restoration time. **RPO** is the maximum acceptable data-loss window. Requirements choose the strategy; the strategy does not choose the requirements.

## Data-tier resilience

- RDS Multi-AZ provides availability and managed failover; it is not the primary read-scaling answer.
- Read replicas serve reads and replicate asynchronously; promotion behavior depends on the engine and design.
- DynamoDB is multi-AZ by design within a Region; global tables add multi-Region replication.
- S3 stores data redundantly across multiple AZs for standard regional storage classes; lifecycle and replication address different requirements.

## Self-check

1. Why does a queue improve resilience during a traffic spike?
2. Which DR option normally matches the lowest RTO with the highest cost?
3. When does a read replica solve a different problem from Multi-AZ?
4. Why should event consumers be idempotent?

<p align="right"><a href="01-secure-architectures.md">← Security</a> · <a href="../README.md">↑ Guide</a> · <a href="03-high-performing-architectures.md">Performance →</a></p>
