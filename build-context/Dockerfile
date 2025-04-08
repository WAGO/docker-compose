FROM alpine:3.21
LABEL authors="<Dirk.Meihoefer@wago.com>,<Sergei.Ikkert@wago.com>"
RUN apk add --no-cache \
    docker-cli-compose
WORKDIR /compose
ENTRYPOINT ["docker-compose"]
