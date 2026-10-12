FROM golang:1.16

WORKDIR /usr/src/app

COPY go.mod go.sum ./
RUN go mod download

COPY . .

RUN go test ./...

RUN go build -o server .

ENV PORT=8080
ENV REQUEST_ORIGIN=https://example.com

EXPOSE $PORT

CMD ["./server"]
