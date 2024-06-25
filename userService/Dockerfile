FROM golang:1.16 as builder
WORKDIR /app
COPY . .
RUN go build -o user-service .

FROM alpine:latest
WORKDIR /root/
COPY --from=builder /app/user-service .
CMD ["./user-service"]
