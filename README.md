# Week 4 - Docker Practical

A hands-on Docker practical project demonstrating containerization, Docker images and containers, Dockerfile-based image creation, persistent volumes, custom networks, Docker Compose, multi-container deployment, and Docker Hub image publishing.

## Environment

- Ubuntu Linux on WSL2
- Docker Engine
- Docker CLI
- Docker Compose

## Application

A simple HTML application is served by Nginx inside a Docker container.

The Docker Compose deployment contains:
- Nginx web service
- Redis service
- Custom bridge network
- Named volume for Nginx logs

## Practical Exercises Completed

### Docker Installation and Verification

Verified Docker Engine with:

```bash
docker --version
docker info
docker run hello-world
```

### Docker Images

Pulled images from Docker Hub and inspected local images:

```bash
docker pull nginx
docker images
```

### Docker Containers

Created and managed containers and exposed the web application through:

```text
http://localhost:8080
```

### Custom Docker Image

Built the project image with:

```bash
docker build -t week4-docker-app:v1 .
```

### Dockerfile

```dockerfile
FROM nginx:alpine

COPY index.html /usr/share/nginx/html/index.html

EXPOSE 80
```

### Docker Volume

Created and tested the named volume:

```text
week4-data
```

Persistence was verified after removing the original container.

### Docker Network

Created a custom bridge network:

```text
week4-network
```

and connected the web container to it.

### Docker Compose

Deployed Nginx and Redis using:

```bash
docker compose up -d --build
docker compose ps
```

Redis was verified with `PONG` and a SET/GET test.

### Docker Hub

Published the custom image:

```text
rajeshkumar357/week4-docker-app:v1
```

## Project Structure

```text
week-4-docker-practical/
├── Dockerfile
├── docker-compose.yml
├── index.html
├── README.md
├── screenshots/
└── report/
    └── Docker_Week4_Report.pdf
```

## Evidence

Required screenshot names:

```text
01-docker-installation.png
02-docker-version.png
03-docker-images.png
04-running-containers.png
05-docker-network.png
06-docker-volume.png
07-compose.png
08-docker-hub.png
```

Screenshots 04–08 are included in the provided asset package. Add your actual screenshots 01–03 before final submission if they are not already available.

## GitHub Repository

https://github.com/Rajeshkumar8967/week-4-docker-practical

## Docker Hub

https://hub.docker.com/r/rajeshkumar357/week4-docker-app
