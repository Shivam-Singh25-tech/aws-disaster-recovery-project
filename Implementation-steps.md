# Implementation Steps – AWS Disaster Recovery

## Phase 1: EC2 Disaster Recovery (Compute Layer)

1. Launched an EC2 instance in Mumbai region
2. Configured security group and key pair
3. Installed application on EC2
4. Created AMI from running instance
5. Verified recovery by launching new EC2 from AMI

---

## Phase 2: RDS Disaster Recovery (Database Layer)

1. Created MySQL RDS instance
2. Enabled automated backups
3. Created manual DB snapshot
4. Restored new RDS instance from snapshot
5. Verified database availability

---

## Phase 3: S3 Disaster Recovery (Storage Layer)

1. Created S3 bucket in Mumbai region
2. Enabled versioning
3. Created S3 bucket in Singapore region
4. Enabled versioning on destination bucket
5. Configured Cross-Region Replication
6. Verified automatic object replication

---

## Cleanup

All AWS resources were deleted after testing to avoid unnecessary costs.
