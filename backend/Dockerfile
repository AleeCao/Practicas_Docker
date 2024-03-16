FROM golang:1.16-alpine

WORKDIR /usr/src/app

EXPOSE 8080

COPY go.mod go.sum ./
RUN go mod download 

COPY . .

RUN go build -o server

ENV REQUEST_ORIGIN=http://localhost:5001

ENV PORT=8080

ENV REDIS_HOST=redisgo

CMD [ "./server" ]