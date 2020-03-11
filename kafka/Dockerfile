FROM centos:7

RUN yum update -y

RUN yum install -y wget java-1.8.0-openjdk-devel

WORKDIR /tmp

RUN wget https://www-eu.apache.org/dist/kafka/2.4.0/kafka_2.12-2.4.0.tgz

RUN chmod +x kafka_2.12-2.4.0.tgz

RUN tar -xzvf kafka_2.12-2.4.0.tgz

RUN mkdir /usr/local/kafka

RUN mv kafka_2.12-2.4.0/* /usr/local/kafka

RUN rm -rf kafka_2.12-2.4.0

WORKDIR /usr/local/kafka

EXPOSE 9092

ENTRYPOINT ["bin/kafka-server-start.sh","config/server.properties"]
