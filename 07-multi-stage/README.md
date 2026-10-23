# Multi-Stage Docker Builds

Multi-stage builds allow Dockerfiles to use multiple `FROM` instructions.

The builder stage contains tools required to build the application.

The final stage contains only the artifacts required to run the application.

## Example

```dockerfile
FROM alpine:latest AS builder

RUN echo "Building application..." > /build-output.txt

FROM alpine:latest

COPY --from=builder /build-output.txt /app/build-output.txt

CMD ["cat", "/app/build-output.txt"]


