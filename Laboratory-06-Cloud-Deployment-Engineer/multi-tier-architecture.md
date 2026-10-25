# Multi-Tier Architecture

## The Web/Application Tier
The Web/Application tier is responsible for serving the user interface and handling HTTP/HTTPS requests from clients. In this deployment, the Nextcloud container acts as the application tier, processing user interactions, managing file uploads, and presenting the web interface.

## The Database Tier
The Database tier is responsible for storing persistent data securely. In this setup, the MariaDB container stores user credentials, file metadata, and application configuration settings, ensuring data remains intact even if the application container restarts.

## Why Separate Them?
Separating the web server and database into two distinct containers follows the principle of separation of concerns. It improves scalability (you can scale the web tier independently of the database), enhances security (the database can be isolated from direct external access), and simplifies maintenance and updates without affecting the entire system.
