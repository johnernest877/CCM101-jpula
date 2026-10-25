# Laboratory 07: Cloud Operations Engineer

## Mission Overview
This mission focuses on the principles of Site Reliability Engineering (SRE) and cloud observability. Instead of just deploying infrastructure, this lab demonstrates how to establish a host system baseline, deploy a containerized web server, generate artificial traffic, and utilize logs and real-time metrics to prove the application is healthy and ready for a traffic surge.

## Objectives
- Utilize native Linux command-line tools to monitor host CPU, Memory, and Disk capacity.
- Deploy a web container and track its real-time performance using Docker metrics.
- Generate web traffic and extract application access logs for analysis.
- Translate raw performance data into a readable technical report using Markdown.

## Monitoring Commands Executed
- `free -h` (Check available RAM)
- `df -h /` (Check root filesystem storage capacity)
- `top` (View active processes and CPU load)
- `docker run -d --name client-website -p 8080:80 nginx` (Deploy Nginx container)
- `curl http://localhost:8080` (Simulate successful web traffic)
- `curl http://localhost:8080/hidden-admin-page` (Simulate a 404 error)
- `docker logs client-website` (Extract application access logs)
- `docker stats` (View real-time container resource consumption)

## Skills Learned
- Establishing hardware performance baselines using Linux CLI tools.
- Simulating web traffic and intentionally triggering HTTP errors for testing.
- Extracting and analyzing containerized application logs to identify specific error codes (e.g., HTTP 404).
- Utilizing real-time metric streams to verify container resource efficiency.