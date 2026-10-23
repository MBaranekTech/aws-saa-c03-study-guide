# Architecture Labs

Most labs can be completed on paper or with diagrams, so no AWS spend is required. If you deploy resources, set a budget first and remove resources afterward.

## Lab 1 — Three-tier multi-AZ design

Design a public web workload with DNS, edge protection, two AZs, private application subnets, and a managed data tier. Label route paths, security boundaries, failure domains, logs, and secrets. Explain why every component exists.

## Lab 2 — IAM policy reasoning

Write a least-privilege policy concept for an application that reads objects under one S3 prefix and decrypts them with one KMS key. Identify the identity policy, bucket policy, key policy, and role trust policy responsibilities. You may use IAM Access Analyzer policy validation without deploying a workload.

## Lab 3 — Decouple a bursty pipeline

Start with a synchronous upload → process → notify workflow. Redesign it using S3 events, queues or event routing, workers, retry policy, dead-letter handling, idempotency, and observability. Describe what happens when processing is slower than ingestion.

## Lab 4 — Meet RTO and RPO

Compare backup/restore, pilot light, warm standby, and active/active for a fictional service. Assign an estimated recovery sequence, data replication choice, test plan, and cost class to each. Then select one for RTO 30 minutes and RPO 5 minutes, stating assumptions.

## Lab 5 — Storage decision matrix

Choose storage for boot volumes, shared Linux files, static website objects, database backups, high-performance Windows files, and seven-year archives. Record access model, durability/availability need, performance, lifecycle, and cost drivers.

## Lab 6 — Cost review

Use the [AWS Pricing Calculator](https://calculator.aws/) to compare one fixed-size design with an elastic design. Include compute, storage, requests, and data transfer assumptions. Identify which assumptions dominate the result and which requirements prevent the absolute cheapest design.
