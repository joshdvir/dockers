FROM ruby:2-alpine

RUN gem install slanger

COPY start.sh /tmp/start.sh

ENTRYPOINT ["/tmp/start.sh"]