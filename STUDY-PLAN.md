# Study Plan

## Fast track: 20 hours

Use this route if you already understand networking, Linux, databases, and basic AWS services.

| Session | Focus | Time |
|---|---|---:|
| 1 | Diagnostic, blueprint, Well-Architected mindset | 1 h |
| 2 | IAM, accounts, network security, encryption | 5 h |
| 3 | Multi-AZ, decoupling, scaling, disaster recovery | 5 h |
| 4 | Compute, storage, databases, networking performance | 4.5 h |
| 5 | Storage, compute, database, and transfer cost | 3.5 h |
| 6 | Timed practice and mistake review | 1 h |

## Foundation route: six weeks

- **Week 1:** IAM, global infrastructure, VPC fundamentals, shared responsibility.
- **Week 2:** encryption, edge security, secure connectivity, multi-account strategy.
- **Week 3:** load balancing, Auto Scaling, queues, events, serverless, containers.
- **Week 4:** storage and database selection; caching and data movement.
- **Week 5:** disaster recovery, performance, pricing models, cost tools.
- **Week 6:** architecture labs, mixed scenarios, timed practice, mistake journal.

## The scenario method

For every question:

1. underline hard requirements: RTO/RPO, latency, access pattern, compliance, budget;
2. identify the failing quality: security, resilience, performance, or cost;
3. eliminate options that violate a requirement;
4. prefer managed, elastic, loosely coupled designs when requirements allow;
5. choose the simplest option that satisfies all requirements—do not over-architect.

## Mistake journal

Record the requirement you missed, why the distractor looked plausible, the discriminating fact, a primary documentation link, and one changed requirement that would make another answer correct.

## Readiness checks

You should be able to explain, without notes:

- Multi-AZ versus multi-Region and RDS Multi-AZ versus read replicas;
- security groups versus NACLs and roles versus users;
- SQS versus SNS versus EventBridge;
- EBS versus EFS versus S3 and their access models;
- ALB versus NLB, CloudFront versus Global Accelerator;
- On-Demand, Spot, Savings Plans, and Reserved Instance trade-offs;
- how RTO and RPO drive disaster-recovery design.
