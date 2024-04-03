FROM golang:1.22-alpine

WORKDIR /go/src/app/

COPY ./app .

RUN apk upgrade --update && \
    apk --no-cache add git gcc musl-dev

RUN go install github.com/cosmtrek/air@latest
CMD ["air", "-c", ".air.toml"]