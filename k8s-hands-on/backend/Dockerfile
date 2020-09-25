FROM golang:1.13 as builder

WORKDIR /app
COPY ./src/main.go .
RUN CGO_ENABLE=0 GOOS=linux GOARCH=386 GOPROXY=https://proxy.golang.org go build -o app ./main.go

FROM alpine:latest

WORKDIR /app
COPY --from=builder /app/app .
CMD ["./app"]
