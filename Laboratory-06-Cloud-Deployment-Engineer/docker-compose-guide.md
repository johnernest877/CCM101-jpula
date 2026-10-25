# Docker Compose Guide

## What does the `services:` block do?
The `services:` block defines the individual containers that make up the application stack. In this file, it defines two services: `database` (running MariaDB) and `app` (running Nextcloud), specifying their images, ports, and environment variables.

## How did the Nextcloud app container know how to find the database container?
Docker Compose automatically creates a default network for all services in the file. Containers can reach each other using their service names as hostnames. The `MYSQL_HOST=database` environment variable tells the Nextcloud app to look for a container named `database` on the internal Docker network.

## What is the difference between `docker run` and `docker-compose up -d`?
`docker run` is used to start a single container manually, requiring long command-line flags for ports, volumes, and environment variables. `docker-compose up -d` reads a declarative YAML file and automatically provisions, networks, and starts multiple interconnected containers in the background (`-d` for detached mode), making it reproducible and much easier to manage (Infrastructure as Code).
