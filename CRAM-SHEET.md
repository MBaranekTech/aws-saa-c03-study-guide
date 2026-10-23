# SAA-C03 Cram Sheet

## Commonly confused pairs

| A | B | Core distinction |
|---|---|---|
| Security group | Network ACL | Stateful resource control vs stateless subnet control |
| IAM role | IAM user | Assumable temporary identity vs long-lived identity |
| SCP | IAM policy | Permission guardrail vs permission grant/deny |
| RDS Multi-AZ | Read replica | Availability/failover vs read scaling |
| SQS | SNS | Queue/buffer vs push fan-out |
| SNS | EventBridge | Pub/sub delivery vs event-bus routing/rules |
| EBS | EFS | Block volume vs shared managed file system |
| S3 | EFS | Object API vs POSIX-like shared filesystem |
| ALB | NLB | Layer 7 HTTP routing vs Layer 4 transport routing |
| CloudFront | Global Accelerator | CDN/cache at edge vs global network acceleration |
| NAT gateway | Internet gateway | Private-subnet outbound translation vs VPC internet route target |
| Direct Connect | Site-to-Site VPN | Dedicated private connectivity vs encrypted internet tunnel |
| RTO | RPO | Time to restore vs acceptable data loss |
| CloudWatch | CloudTrail | Metrics/logs/alarms vs AWS API activity history |
| WAF | Shield | Web request filtering vs DDoS protection |

## Architecture defaults—not absolutes

- Prefer roles and temporary credentials.
- Spread production tiers across AZs.
- Keep compute stateless and scale horizontally when practical.
- Decouple variable-rate producers and consumers.
- Choose storage/database from access patterns.
- Use managed services when they satisfy control requirements.
- Cache repeated work, but define invalidation and consistency.
- Encrypt data, restrict access, log important actions, and test recovery.
- Optimize after measuring; simpler is often cheaper and more reliable.

## Exam timing

65 questions in 130 minutes gives an average of two minutes per question. Read the final sentence first, identify every hard constraint, eliminate solutions that fail one constraint, and flag long calculations or ambiguous multi-response items for review. There is no penalty for guessing.
