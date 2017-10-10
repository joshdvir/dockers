FROM sonatype/nexus3:3.6.0

USER root

ADD https://bin.equinox.io/c/ekMN3bCZFUn/forego-stable-linux-amd64.rpm /tmp/
RUN rpm -i /tmp/forego-stable-linux-amd64.rpm && rm -fr /tmp/forego-stable-linux-amd64.rpm

RUN echo $'#!/bin/bash\n\
\n\
while true; do\n\
  aws s3 sync $DATA_FOLDER/ s3://$S3_BUCKET/ \n\
  sleep $(( 60*60*INTERVAL_IN_HOURS ))\n\
done' > s3.sh && chmod +x s3.sh

RUN echo 'nexus: bin/nexus run' > Procfile
RUN echo 's3: ./s3.sh' >> Procfile

RUN yum update -y && yum install epel-release -y && yum install python-pip -y && pip install --upgrade pip awscli

USER nexus

ENV INTERVAL_IN_HOURS=1

CMD [ "forego", "start" ]
