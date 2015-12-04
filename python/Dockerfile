FROM alpine:3.2
MAINTAINER Shuky Dvir <shuky@devops.co.il>

RUN apk add --update \
  python \
  python-dev \
  py-pip \
  bash \
  && rm -rf /var/cache/apk/*

CMD ["python --version"]
