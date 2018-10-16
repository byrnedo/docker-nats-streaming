# Nats Streaming on Alpine Linux

The [official](https://github.com/nats-io/nats-streaming-docker) docker image is based on scratch. This makes it hard to do things like this:

```sh
docker run ...  --entrypoint "echo \$NATS_CONFIG > /stan.conf && exec '/nats-streaming-server -c /stan.conf $@'" ...
```

This image is based on alpine so you can do things like that :)

Check it out on [docker hub](https://hub.docker.com/r/byrnedo/alpine-nats-streaming/).
