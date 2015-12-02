FROM alpine:3.2
MAINTAINER Shuky Dvir <shuky@devops.co.il>

RUN apk add --update \
  ruby \
  ruby-io-console \
  bash \
  && rm -rf /var/cache/apk/*

EXPOSE 4568

RUN gem install fake_sqs --no-rdoc --no-ri

CMD [ "/usr/bin/fake_sqs", "-p", "4568", "--no-daemonize" ]