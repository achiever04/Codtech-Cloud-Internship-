# Task 4: Cloud Security – GCP & AWS

## Objective
To implement basic cloud security principles across Google Cloud Platform (GCP) and Amazon Web Services (AWS), focusing on **least privilege**, **firewall configuration**, and **resource access logging**.

---

## Security Measures Implemented

### ✅ GCP – IAM User with Least Privilege
- Created a GCP IAM user
- Granted the `Storage Viewer` role only
- ✅ This user can view but **not delete/upload** files in GCS buckets

> Screenshots:
- `IAM Assign.png`
- `IAM-role-assign.png`

---

### ✅ AWS – Firewall (Security Group) Hardening
- Verified and edited inbound rules for EC2
- Only allowed:
  - **Port 22 (SSH)**
  - **Port 80 (HTTP)**
- Removed access to all other ports

> Screenshot: `security-group.png`

---

### ✅ GCP – Secured Cloud Storage Bucket + Enabled Access Logging
- Removed all public access from the bucket
- Granted object-level view access to specific IAM user only
- Enabled **access logs and storage logs** for auditing activity

> Screenshots:
- `private-bucket.png`
- `bucket-logs.png`

---

## Outcome
This setup ensures:
- **Least privilege principle is enforced**
- **Attack surface is minimized** by closing unused ports
- **Actions are auditable** via logging

---

## Tools Used
- **Google Cloud IAM & Storage**
- **AWS EC2 Security Groups**
