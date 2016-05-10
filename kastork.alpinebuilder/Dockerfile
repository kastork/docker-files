FROM: alpine:edge

COPY repositories /etc/apk/repositories

RUN apk add --update make \
  && apk add --update gcc \
  && apk add --update g++ \
  && apk add --update git \
  && apk add --update bash

RUN rm -rf /var/cache/apk/*
