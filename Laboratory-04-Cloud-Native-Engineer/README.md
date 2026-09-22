# Laboratory 04 - Cloud-Native Engineer

## Mission Overview

This laboratory introduced cloud-native engineering through Docker containers. I compared virtual machines and containers, used a Docker-enabled Ubuntu environment in KillerCoda, deployed an Nginx web server, and managed its container lifecycle.

## Objectives

- Differentiate Virtual Machines and Containers.
- Verify that Docker is installed and running.
- Pull and run an Nginx container.
- Map a host port to a container port.
- Test a containerized web server using a local HTTP request.
- Stop and remove a Docker container.
- Document Docker commands and evidence in GitHub.

## Docker Commands Executed

```bash
docker --version
docker info
docker pull nginx
docker run -d --name nginx-server -p 8080:80 nginx
curl http://localhost:8080
docker ps
docker stop nginx-server
docker ps
docker rm nginx-server
```

## Skills Learned

- Comparing containerization with traditional virtualization.
- Using Docker commands in a Linux terminal.
- Downloading Docker images from Docker Hub.
- Running an Nginx web server in a container.
- Mapping port `8080` on the host to port `80` inside the container.
- Managing the lifecycle of a Docker container.
- Organizing technical documentation and screenshots in GitHub.

## Challenges Encountered

One challenge was understanding how port mapping works between the host and a container. I solved this by using `-p 8080:80` and confirming the result with `curl http://localhost:8080`. I also learned that a stopped container still exists until it is removed with `docker rm`.
