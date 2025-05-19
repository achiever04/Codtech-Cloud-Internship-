# Task 2: Cloud Monitoring and Alerting – Google Cloud

## Objective
To monitor a Compute Engine VM instance using Google Cloud Monitoring and set up alerting for high CPU usage and service availability.

---

## Resources Monitored
- **VM Instance:** `codtech-monitor-vm`
- **Metrics Tracked:**
  - CPU Utilization
  - Disk Read Bytes
  - Network Received Bytes
  - Uptime

---

## Cloud Ops Agent
Installed the Google Cloud Ops Agent on the VM using:

```bash
curl -sSO https://dl.google.com/cloudagents/add-google-cloud-ops-agent-repo.sh
sudo bash add-google-cloud-ops-agent-repo.sh --also-install
