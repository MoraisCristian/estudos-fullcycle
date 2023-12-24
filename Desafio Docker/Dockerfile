# Start from a Debian-based image with the Go language installed
FROM golang:latest AS builder

WORKDIR /app

COPY ./main.go .

RUN go mod init full-cycle/desafio

RUN go build main.go

FROM scratch

COPY --from=builder /app/main .

CMD [ "./main" ]

