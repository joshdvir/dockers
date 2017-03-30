FROM ubuntu:latest
LABEL maintainer="Josh Dvir - josh@dvir.uk" \
      io.whalebrew.name="saws" \
      io.whalebrew.config.volumes='["~/.aws:/root/.aws:ro"]'

RUN apt-get update && apt-get install -y \
    groff \
    python-pip \
  && apt-get clean \
  && rm -rf /var/lib/apt/lists/*

RUN mkdir -p /workdir
WORKDIR /workdir

RUN pip install saws

ENTRYPOINT ["saws"]