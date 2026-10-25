# Mission Reflection

Checking the host server's resources is critical because containers share the host's underlying kernel and hardware. Even if a container appears to be running perfectly, a host-level resource exhaustion (like a full disk or out-of-memory condition) will inevitably crash all containers running on that machine. 

If a user complains they cannot log into a web application, the `docker logs` command is the first place I would look. It acts as a security camera, showing the exact HTTP requests hitting the server. I could search the logs for the user's specific action or look for HTTP 500 (Internal Server Error) or 401 (Unauthorized) codes to pinpoint whether the issue is a bad password, a database connection failure, or an application bug.

The difference between monitoring logs and monitoring metrics is that logs provide a chronological, detailed narrative of discrete events (the "what" and "why" something happened), while metrics provide quantitative, real-time numerical data about system health (the "how much" or "how fast," like CPU percentage or memory usage). 

Large enterprise companies monitor thousands of containers simultaneously using centralized observability stacks. Instead of running `docker stats` manually, they deploy tools like Prometheus to scrape and store time-series metrics from all nodes, and Grafana to visualize that data on unified dashboards. They also use log aggregators like the ELK stack (Elasticsearch, Logstash, Kibana) or Fluentd to centralize logs from every container into one searchable interface.

Since Mission 1, my ability to troubleshoot Linux environments has improved significantly. I no longer just guess what is wrong; I now know how to systematically check disk space, monitor live processes, and read container logs to find concrete evidence of a problem, transitioning from a passive user to a proactive Cloud Operations Engineer.