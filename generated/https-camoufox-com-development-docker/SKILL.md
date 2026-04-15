---
name: docker
description: Use this skill when working with Docker. Triggers when user mentions Docker or imports from it.
---

# Docker

## What this is
Docker is a containerization platform that allows developers to package, ship, and run applications in containers. Containers are lightweight and portable, enabling consistent and reliable deployments across different environments. Docker provides a simple and efficient way to manage applications and their dependencies.

## Installation
```bash
curl -fsSL https://get.docker.com -o get-docker.sh
sh get-docker.sh
```

## Key concepts
The most important APIs and patterns in Docker include:
* **Images**: Templates for creating containers. Example: `docker pull ubuntu` to pull the Ubuntu image.
* **Containers**: Isolated environments for running applications. Example: `docker run -it ubuntu` to run a new container from the Ubuntu image.
* **Volumes**: Shared file systems between containers and the host machine. Example: `docker run -v /host/path:/container/path ubuntu` to mount a volume.
* **Networking**: Communication between containers. Example: `docker network create my-network` to create a new network.

## Correct usage patterns
Real code examples from the Docker documentation include:
* Running a new container: `docker run -it ubuntu /bin/bash`
* Building a Docker image: `docker build -t my-image .`
* Pushing an image to Docker Hub: `docker tag my-image:latest <username>/my-image:latest` and `docker push <username>/my-image:latest`

## Common mistakes to avoid
Common mistakes when using Docker include:
* Not specifying the correct port mappings when running a container.
* Not using volumes to persist data between container restarts.
* Not optimizing Docker images for size and performance.

## File and folder conventions
Docker files and folders typically follow these conventions:
* **Dockerfile**: The build file for a Docker image, usually located in the root of the project directory.
* **docker-compose.yml**: The configuration file for defining and running multi-container applications, usually located in the root of the project directory.
* **.dockerignore**: The file specifying files and directories to ignore during the build process, usually located in the root of the project directory.