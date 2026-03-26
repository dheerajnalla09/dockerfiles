# Stage 1: Build
FROM golang:1.21 AS build
WORKDIR /app
COPY . .
RUN go build -o /myapp ./cmd

# Stage 2: Final image
FROM almalinux:9
COPY --from=build /myapp /usr/bin/myapp
EXPOSE 8080
CMD ["/usr/bin/myapp"]