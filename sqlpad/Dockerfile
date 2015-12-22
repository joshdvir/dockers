FROM mhart/alpine-node

RUN apk add --update \
    bash

RUN npm install sqlpad -g

ENV NODE_ENV=production

RUN mkdir -p /data

VOLUME ["/data"]

ENTRYPOINT ["sqlpad --dir /data"]