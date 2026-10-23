# Original Practice Questions

Choose the best answer unless the question says **Choose two**. Suggested time: 40 minutes. These are original learning scenarios, not recalled exam content.

1. EC2 instances need to read one S3 bucket without stored access keys. What is best? A) IAM user keys in user data B) Instance role with least privilege C) Root credentials D) Public bucket
2. A private-subnet workload needs supported S3 access without NAT or internet traversal. What should be evaluated first? A) Internet gateway B) VPC endpoint C) Elastic IP D) CloudFront
3. Which statement is correct? A) NACLs are stateful B) Security groups support deny rules C) Security groups are stateful D) NACLs attach to IAM roles
4. An order API receives sudden bursts, but workers process at a steady rate. What improves resilience? A) SQS between API and workers B) Larger DNS TTL C) One larger worker D) Disable retries
5. One event must immediately reach independent billing, analytics, and notification consumers. What pattern fits? A) One SQS queue with competing consumers B) SNS fan-out, commonly to separate queues C) EBS snapshots D) NAT gateway
6. A relational database needs automatic failover across AZs. Read traffic is modest. Choose: A) Read replica only B) RDS Multi-AZ C) ElastiCache only D) S3 replication
7. A relational database is healthy but overwhelmed by repeat read queries. Choose: A) Multi-AZ standby B) Read replica or cache based on consistency needs C) More NAT gateways D) Glacier
8. Many Linux EC2 instances require concurrent access to the same managed POSIX-style filesystem. Choose: A) EBS B) EFS C) Instance store D) SQS
9. A global website serves mostly static objects from S3. Lowest-latency delivery? A) CloudFront B) Direct Connect C) Transit Gateway D) EBS
10. Which control can explicitly deny traffic at subnet level? A) Security group B) Network ACL C) IAM role D) KMS key
11. A batch renderer can tolerate interruption and retries. Cheapest compute model to evaluate? A) Dedicated Hosts only B) Spot Instances C) On-Demand only D) Provisioned IOPS
12. The business allows four hours to restore service and one hour of data loss. Which values are these? A) RPO 4h, RTO 1h B) RTO 4h, RPO 1h C) TTL and MTU D) IOPS and throughput
13. An application must route `/api` and `/images` to different target groups. Choose: A) NLB B) ALB C) NAT gateway D) Direct Connect
14. **Choose two.** Which improve a stateless web tier's AZ resilience? A) Auto Scaling group across AZs B) ALB across AZs C) One large instance D) Local-only session files E) One-AZ database with no backup
15. A workload needs audit history of AWS API calls. Choose: A) CloudWatch metrics only B) CloudTrail C) ElastiCache D) Route 53 Resolver
16. A team needs an alarm when estimated monthly spend crosses a threshold. Choose: A) AWS Budgets B) AWS WAF C) AWS DMS D) Inspector
17. Which DR strategy keeps a scaled-down working environment? A) Backup and restore B) Pilot light C) Warm standby D) No backup
18. A Lambda function opens too many short-lived RDS connections. What should be evaluated? A) RDS Proxy B) S3 Transfer Acceleration C) Shield D) EFS lifecycle
19. A public web app needs filtering for SQL injection and common HTTP exploits. Choose: A) AWS WAF B) NACL only C) KMS D) Cost Explorer
20. An architecture saves cross-AZ fees by placing every component in one AZ, violating the availability requirement. Is it cost optimized? A) Yes, lowest bill always wins B) No, it fails a requirement and ignores failure cost C) Yes, AZs never fail D) No, because multi-Region is always required

---

**Finished?** [Read the explanations →](answers.md)
