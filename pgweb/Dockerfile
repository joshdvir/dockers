FROM alpine

RUN apk --no-cache add wget unzip ca-certificates

RUN mkdir -p /app
WORKDIR /app

ENV PGWEB_VERSION 0.9.6

RUN \
  cd /tmp && \
  wget https://github.com/sosedoff/pgweb/releases/download/v$PGWEB_VERSION/pgweb_linux_amd64.zip && \
  unzip pgweb_linux_amd64.zip -d /app && \
  rm -f pgweb_linux_amd64.zip

ENTRYPOINT ["/app/pgweb_linux_amd64"]
CMD ["-s", "--bind=0.0.0.0", "--listen=8080"]
