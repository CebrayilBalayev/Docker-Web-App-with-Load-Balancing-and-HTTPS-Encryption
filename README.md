# Docker-Web-App-with-Load-Balancing-and-HTTPS-Encryption

This is a containerized web application with load balancing and HTTPS encryption. The application consists of two web pages that are distributed across multiple servers using a load balancer container. The application also includes a certificate container that enables HTTPS encryption for secure communication between the web pages and the clients. The entire application is deployed and managed using Docker Compose, which provides a simple and efficient way to orchestrate the containers and automate the deployment process.

> docker compose build
> docker compose up -d

when you are done
> docker compose down -v
