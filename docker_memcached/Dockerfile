FROM alpine:3.2
MAINTAINER Shuky Dvir <shuky@devops.co.il>

RUN apk add --update \
  memcached \
  && rm -rf /var/cache/apk/*

EXPOSE 11211

CMD ["/usr/bin/memcached", "-u", "root", "-vvv"]
