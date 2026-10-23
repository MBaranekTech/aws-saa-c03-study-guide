# Domain 4 — Design Cost-Optimized Architectures (20%)

> **Outcome:** Meet requirements at the lowest sustainable cost by matching pricing, capacity, storage, database, and network choices to actual usage.

## Cost is an architecture property

Optimize total cost, not one line item. Include compute, storage, requests, licenses, support, data transfer, operations, and failure impact. Measure first; right-size and remove waste; then commit to discounts for understood baseline usage.

## Compute purchasing models

| Model | Best fit |
|---|---|
| On-Demand | Uncertain, short-lived, or changing workloads |
| Spot | Interruptible, flexible, fault-tolerant work |
| Savings Plans | Predictable compute commitment with model-specific flexibility |
| Reserved Instances | Eligible steady-state instance usage and, for some offerings, capacity needs |

Auto Scaling matches supply to demand. Serverless can reduce idle capacity, but request volume, duration, concurrency, and surrounding services determine real cost.

## Storage and data lifecycle

Select storage class from access frequency, retrieval time, minimum duration, and retrieval cost. Use lifecycle policies when data age predicts access. Delete obsolete snapshots and unattached resources only after validating retention needs.

S3 Intelligent-Tiering helps when object access patterns are unknown or change, subject to its pricing details. EBS type and provisioned performance should match measured needs.

## Database cost

Right-size instances/capacity, use serverless modes when the demand pattern fits, and avoid unnecessary replicas. DynamoDB on-demand fits unpredictable traffic; provisioned capacity can fit predictable traffic. Caching may reduce expensive database work but introduces its own cost and consistency considerations.

## Network cost

Data transfer paths matter. Keep chatty components near each other when resilience permits, cache content at the edge, compress payloads, and evaluate NAT gateway processing versus appropriate VPC endpoints. Never sacrifice required fault isolation merely to avoid cross-AZ cost.

## Cost tools

- Cost Explorer analyzes spend and usage trends.
- AWS Budgets tracks thresholds and forecasts with alerts/actions.
- Cost and Usage Report provides detailed billing data.
- Compute Optimizer recommends resource adjustments from utilization signals.
- Pricing Calculator estimates proposed architecture cost.

## Self-check

1. Why should commitment discounts usually follow right-sizing?
2. Which workload traits make Spot appropriate?
3. When can a VPC endpoint reduce both exposure and NAT processing cost?
4. Why is the cheapest single-AZ design not automatically cost optimized?

<p align="right"><a href="03-high-performing-architectures.md">← Performance</a> · <a href="../README.md">↑ Back to guide</a></p>
