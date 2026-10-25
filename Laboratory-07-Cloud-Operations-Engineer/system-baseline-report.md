# System Baseline Report

## Host Resource Metrics
- **Total RAM Available:** [Insert the "total" value from the `free -h` command, e.g., 3.8Gi]
- **Total Root (/) Storage Capacity:** [Insert the "Size" value from the `df -h /` command, e.g., 50G]

## Why Disk Space Matters
Checking disk space before a massive traffic surge is critical because web servers generate access logs, temporary files, and cache data; if the disk fills up, the application will crash and new users will be unable to connect.