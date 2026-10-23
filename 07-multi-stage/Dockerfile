# Stage 1: Builder
FROM alpine:latest AS builder

RUN echo "Building application..." > /build-output.txt


# Stage 2: Production
FROM alpine:latest

COPY --from=builder /build-output.txt /app/build-output.txt

CMD ["cat", "/app/build-output.txt"]


