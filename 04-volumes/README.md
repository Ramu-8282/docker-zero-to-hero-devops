# Docker Volumes

## Why Volumes?

Container filesystems are ephemeral. Data can be lost when a container is removed.

Docker volumes provide persistent storage independent of the container lifecycle.

## Create Volume

```bash
docker volume create devops-data


