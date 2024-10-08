FROM golang:1.21.0 AS builder

WORKDIR /app

COPY . .

RUN go build -o fullcycle

FROM golang:alpine

COPY --from=builder /app/fullcycle /fullcycle

ENTRYPOINT ["/fullcycle"]