# Docker Compose

Docker Compose allows multiple containers and their configuration to be defined in a single YAML file.

## Example

```yaml
services:

  web:
    image: nginx:latest
    ports:
      - "8082:80"

  app:
    image: alpine:latest


