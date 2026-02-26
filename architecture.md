# AWS Disaster Recovery Architecture

## Overview

This architecture implements a 3-layer disaster recovery strategy:

1. Compute Layer Backup (EC2 AMI)
2. Database Layer Backup (RDS Snapshot)
3. Storage Layer Replication (S3 Cross-Region Replication)

## Flow Diagram

Users → EC2 (Mumbai) → RDS (Mumbai) → S3 (Mumbai) → Replicated to S3 (Singapore)

## Disaster Scenario

If Mumbai region fails:

- EC2 can be restored using AMI
- RDS can be restored from snapshot
- S3 data is available in Singapore region
