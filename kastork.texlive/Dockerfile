from alpine:edge

COPY repositories /etc/apk/repositories

RUN apk add --update texlive-full \
  && rm -rf /var/cache/apk/*

WORKDIR /source
VOLUME /source


