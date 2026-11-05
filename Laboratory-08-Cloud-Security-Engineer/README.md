# Laboratory 08: Cloud Security Engineer

## Mission Overview
This mission focuses on securing a cloud server using host-based firewalls. Acting as a Cloud Security Engineer, I deployed a web application and used the Uncomplicated Firewall (UFW) to lock down the server, enforcing a strict Default Deny policy while selectively allowing necessary traffic for SSH and the web application.

## Objectives
- Understand the concept of the Attack Surface and the Principle of Least Privilege (PoLP).
- Perform a basic security audit of active network ports on a Linux server.
- Configure the Uncomplicated Firewall (UFW) with a Default Deny policy.
- Implement granular port management to selectively allow SSH and HTTP traffic.
- Document firewall rules and security best practices using Markdown.

## Commands Executed
- `docker run -d --name secure-web-app -p 8080:80 nginx` (Deploy Nginx container)
- `curl http://localhost:8080` (Verify web app is reachable)
- `sudo ufw allow ssh` (Allow SSH access to prevent lockout)
- `sudo ufw default deny incoming` (Block all incoming traffic by default)
- `sudo ufw default allow outgoing` (Allow all outgoing traffic)
- `sudo ufw enable` (Activate the firewall)
- `sudo ufw status verbose` (Check firewall status)
- `sudo ufw allow 8080/tcp` (Open port for web traffic)
- `sudo ufw status numbered` (Verify firewall rules)

## Skills Learned
- Implementing the Principle of Least Privilege by only opening necessary ports.
- Configuring a host-based firewall (UFW) to protect a Linux server.
- Understanding the critical importance of allowing SSH before enabling a firewall.
- Documenting security configurations and audit procedures professionally.