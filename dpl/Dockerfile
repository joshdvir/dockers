FROM ruby:2.3
MAINTAINER Shuky Dvir <shuky@devops.co.il>

RUN apt-get update \
    && apt-get install -y zip \
    && gem install dpl aws-sdk --no-ri --no-rdoc

CMD ["ruby", "-v"]
