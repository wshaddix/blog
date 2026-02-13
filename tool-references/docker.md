---
title: Docker CLI
order: 3
---

# Docker CLI Reference

Quick reference for common Docker commands.

## Images

```bash
# List images
docker images

# Pull an image
docker pull mcr.microsoft.com/dotnet/aspnet:8.0

# Build an image
docker build -t myapp:latest .

# Remove an image
docker rmi myapp:latest
```

## Containers

```bash
# Run a container
docker run -d -p 8080:80 --name myapp myapp:latest

# List running containers
docker ps

# List all containers
docker ps -a

# Stop a container
docker stop myapp

# Remove a container
docker rm myapp

# View logs
docker logs myapp
docker logs -f myapp  # Follow

# Execute command in container
docker exec -it myapp /bin/bash
```

## Docker Compose

```bash
# Start services
docker compose up -d

# Stop services
docker compose down

# View logs
docker compose logs -f

# Rebuild and restart
docker compose up -d --build
```

## Cleanup

```bash
# Remove stopped containers
docker container prune

# Remove unused images
docker image prune

# Remove all unused objects
docker system prune

# Nuclear option - remove everything
docker system prune -a --volumes
```

---

See [DevOps: Containerization](/devops/containerization/docker-fundamentals) for detailed Docker guides.
