FROM docker:17.05-git

RUN apk update && apk add \
      bash \
      curl \
      less \
      groff \
      jq \
      ca-certificates \
      python \
      py-pip \
      py2-pip && \
      pip install --upgrade pip awscli

RUN curl -Lo /usr/local/bin/kubectl https://storage.googleapis.com/kubernetes-release/release/$(curl -s https://storage.googleapis.com/kubernetes-release/release/stable.txt)/bin/linux/amd64/kubectl

RUN chmod +x /usr/local/bin/kubectl