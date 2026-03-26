# Stage 1: name this stage "build"
FROM golang:1.21 AS build
WORKDIR /app
COPY . .
RUN go build -o /myapp ./cmd

# Stage 2: final image
FROM almalinux:9
COPY --from=build /myapp /usr/bin/   # ✅ now correctly references stage 1
CMD ["/usr/bin/myapp"]