# Stage 1: name this stage "build"
FROM golang:1.21 AS build
WORKDIR /app
COPY . .
RUN go build -o /myapp ./cmd
