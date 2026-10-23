# Domain 3 — Design High-Performing Architectures (24%)

<p align="center"><img src="../assets/performance-cost.png" alt="Elastic cloud resources adapting to changing demand through caches, compute, databases, and tiered storage" width="100%"></p>

> **Outcome:** Select compute, storage, database, and network designs that meet measurable performance requirements.

## Compute selection

- EC2 offers instance-level control and many hardware profiles.
- Lambda fits event-driven, short-lived, stateless execution within service limits.
- Fargate runs containers without managing worker instances.
- ECS and EKS orchestrate containers; choose based on ecosystem and operational requirements.
- Auto Scaling and load balancing address elasticity and healthy traffic distribution.

Choose based on workload shape, duration, state, startup characteristics, concurrency, hardware, and operational control—not fashion.

## Storage selection

| Need | First service family to evaluate |
|---|---|
| Durable object storage and massive scale | S3 |
| Block device for an instance | EBS |
| Shared POSIX file system for Linux workloads | EFS |
| Specialized managed file system | FSx family |
| Archive with retrieval trade-offs | S3 Glacier classes |

Performance depends on access pattern: throughput, IOPS, latency, object size, concurrency, metadata behavior, and locality.

## Database selection

- RDS/Aurora: relational transactions, SQL, joins, and established engines.
- DynamoDB: predictable key-based access at large scale with managed capacity.
- ElastiCache: microsecond-scale in-memory caching to offload durable stores.
- Redshift: analytical warehouse queries.
- OpenSearch Service: search and log analytics.

Indexes and access patterns matter more than category names. Use replicas for read scale, caches for repeated reads, and connection proxies where connection storms are the bottleneck.

## Network and edge

- CloudFront caches content at edge locations and can front HTTP origins.
- Global Accelerator uses the AWS global network to improve availability/performance for supported TCP/UDP endpoints.
- ALB provides Layer 7 HTTP routing; NLB provides high-performance Layer 4 load balancing and static IP-related capabilities.
- Direct Connect provides dedicated connectivity; VPN provides encrypted connectivity over the internet. They can be combined for requirements.

## Self-check

1. Why is EFS a better first candidate than EBS for shared Linux file access across instances?
2. When does CloudFront solve a different problem from Global Accelerator?
3. What requirement favors DynamoDB over an RDS engine?
4. Why can caching improve both performance and cost?

<p align="right"><a href="02-resilient-architectures.md">← Resilience</a> · <a href="../README.md">↑ Guide</a> · <a href="04-cost-optimized-architectures.md">Cost →</a></p>
