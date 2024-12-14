FROM alpine:latest
RUN echo "Hello, world!" > /app/hello.txt
CMD ["cat", "/app/hello.txt"]