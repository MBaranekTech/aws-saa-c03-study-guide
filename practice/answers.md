# Answers and Explanations

1. **B.** An instance role supplies temporary credentials without embedding secrets.
2. **B.** An appropriate VPC endpoint keeps supported service traffic on private connectivity and can avoid NAT processing.
3. **C.** Security groups are stateful; NACLs are stateless and support allow and deny rules.
4. **A.** SQS buffers the burst and lets workers consume at a sustainable rate.
5. **B.** Fan-out delivers the same event to independent subscribers; separate queues add durable buffering per consumer.
6. **B.** Multi-AZ addresses managed availability and failover. A read replica primarily addresses read scale.
7. **B.** Replicas scale eligible reads; a cache can avoid repeated database work when consistency permits.
8. **B.** EFS provides a managed shared file system. EBS is block storage generally attached within its supported model.
9. **A.** CloudFront caches and delivers content from edge locations close to users.
10. **B.** NACLs operate at subnet boundaries and can contain explicit deny rules.
11. **B.** Spot fits interruption-tolerant, retryable workloads when interruption handling is designed in.
12. **B.** RTO is restoration time; RPO is acceptable data loss.
13. **B.** ALB supports content-based Layer 7 routing.
14. **A and B.** Multi-AZ Auto Scaling and load balancing remove single-instance/AZ dependence in the web tier.
15. **B.** CloudTrail records AWS API activity. CloudWatch handles monitoring signals such as metrics, logs, and alarms.
16. **A.** Budgets tracks cost/usage thresholds and forecasts with notifications or supported actions.
17. **C.** Warm standby maintains a functional but scaled-down environment.
18. **A.** RDS Proxy pools and manages database connections for supported engines and patterns.
19. **A.** WAF evaluates HTTP(S) requests against managed or custom web rules.
20. **B.** Cost optimization means meeting requirements efficiently, not minimizing the bill while discarding resilience.

## Score guide

- **17–20:** strong foundation; verify every uncertain answer and practice longer multi-constraint scenarios.
- **13–16:** good start; revisit the corresponding domain for every miss.
- **0–12:** study all four domains and complete the architecture labs before another timed set.

This short quiz is not an exam predictor and does not cover every in-scope service.
