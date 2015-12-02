FROM alpine:3.2
MAINTAINER Shuky Dvir <shuky@devops.co.il>

RUN apk add --update \
  ruby \
  ruby-io-console \
  bash \
  && rm -rf /var/cache/apk/*

EXPOSE 3000

RUN gem install fake_sns --no-rdoc --no-ri

CMD [ "/usr/bin/fake_sns", "-p", "3000", "--no-daemonize" ]