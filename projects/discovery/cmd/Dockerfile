FROM alpine:3.13.8

ARG GOARCH=amd64

# Needed for access to AWS
RUN apk upgrade --update-cache \
    && apk add ca-certificates \
    && rm -rf /var/cache/apk/*

COPY discovery-linux-$GOARCH /usr/local/bin/discovery

USER 10101

ENTRYPOINT ["/usr/local/bin/discovery"]