# Docker Deployment and Container Lifecycle

## Deploying Nginx

```bash
docker pull nginx
```

This downloaded the official Nginx image from Docker Hub to the Docker environment.

```bash
docker run -d --name nginx-server -p 8080:80 nginx
```

This created and started an Nginx container in detached mode, named it `nginx-server`, and mapped host port 8080 to container port 80.

```bash
curl http://localhost:8080
```

This sent a local request to the Nginx web server and returned the "Welcome to nginx!" page, confirming that the container was working.

## Container Lifecycle

```bash
docker ps
```

This listed the running containers and showed that `nginx-server` was active.

```bash
docker stop nginx-server
```

This stopped the running Nginx container.

```bash
docker ps
```

This verified that no containers were running after `nginx-server` was stopped.

```bash
docker rm nginx-server
```

This permanently removed the stopped `nginx-server` container.
