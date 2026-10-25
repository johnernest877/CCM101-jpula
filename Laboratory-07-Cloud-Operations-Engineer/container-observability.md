# Container Observability Report

## Application Log Analysis

**The 404 Error Log Line:**
```text
172.17.0.1 - - [25/Oct/2026:08:21:38 +0000] "GET /hidden-admin-page HTTP/1.1" 404 153 "-" "curl/8.5.0" "-"
```

**Why Application Logs are Vital:**
Application logs provide a chronological, detailed record of every request and error that occurs inside a container. When a user reports an issue, these logs allow engineers to pinpoint the exact time, endpoint, and nature of the failure, turning a vague "it's broken" complaint into a solvable technical problem.

---

## Real-Time Container Metrics

**Client-Website Container Resource Consumption:**
- **Memory Usage:** 2.727MiB
- **CPU Percentage:** 0.00%