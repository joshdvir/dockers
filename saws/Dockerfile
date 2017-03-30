FROM python:3.6-alpine
LABEL maintainer="Josh Dvir - josh@dvir.uk" \
      io.whalebrew.name="saws" \
      io.whalebrew.config.volumes='["~/.aws:/root/.aws"]'

RUN mkdir -p /workdir
WORKDIR /workdir

RUN pip install saws

ENTRYPOINT ["saws"]
