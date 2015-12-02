FROM alpine:edge
MAINTAINER Shuky Dvir <shuky@devops.co.il>

RUN echo http://dl-4.alpinelinux.org/alpine/edge/testing >> /etc/apk/repositories
RUN apk add --update \
  mongodb \
  && rm -rf /var/cache/apk/*

RUN mkdir -p /data/db && chown -R mongodb /data/db

VOLUME /data/db

EXPOSE 27017 28017

CMD ["mongod"]
