FROM sonatype/nexus3:3.15.2

ENV NEXUS_HOME /opt/sonatype/nexus

USER root

RUN yum update -y && yum install epel-release -y && yum install python-pip unzip -y && pip install --upgrade pip awscli

ADD https://bin.equinox.io/c/ekMN3bCZFUn/forego-stable-linux-amd64.rpm /tmp/
RUN rpm -i /tmp/forego-stable-linux-amd64.rpm && rm -fr /tmp/forego-stable-linux-amd64.rpm

RUN chmod +x /usr/local/bin/forego

RUN echo $'#!/bin/bash\n\
\n\
while true; do\n\
  aws s3 sync $DATA_FOLDER/ s3://$S3_BUCKET/ \n\
  sleep $(( 60*60*INTERVAL_IN_HOURS ))\n\
done' > s3.sh && chmod +x s3.sh

RUN echo 'nexus: /opt/sonatype/start-nexus-repository-manager.sh' > Procfile
RUN echo 's3: ./s3.sh' >> Procfile

USER nexus

ENV INTERVAL_IN_HOURS=12

CMD [ "forego", "start" ]

