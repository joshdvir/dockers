FROM anapsix/alpine-java:jre8

WORKDIR /elasticmq
RUN wget https://s3-eu-west-1.amazonaws.com/softwaremill-public/elasticmq-server-0.8.12.jar -O elasticmq-server.jar
COPY config.conf /elasticmq/config.conf
COPY logback.xml /elasticmq/logback.xml

EXPOSE 80

ENTRYPOINT ["java", "-Dconfig.file=/elasticmq/config.conf", "-Dlogback.configurationFile=/elasticmq/logback.xml", "-jar", "/elasticmq/elasticmq-server.jar"]
