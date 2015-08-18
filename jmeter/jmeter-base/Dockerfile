FROM ubuntu:14.04

MAINTAINER luisperlazaro@gmail.com

ENV JDK_PACKAGE openjdk-7-jdk
ENV JMETER_VERSION 2.13
ENV JMETER_MIRROR http://www.eu.apache.org/dist/jmeter/binaries/
ENV JMETER_DOWNLOAD_URL $JMETER_MIRROR/apache-jmeter-$JMETER_VERSION.tgz
ENV BASE_DIR /var/lib
ENV JMETER_HOME $BASE_DIR/apache-jmeter-$JMETER_VERSION

RUN \
    apt-get update && \
    apt-get -y install $JDK_PACKAGE curl

# Install jmeter
RUN curl $JMETER_DOWNLOAD_URL -o /tmp/jmeter-$JMETER_VERSION.tgz && \
    cd $BASE_DIR && tar xf /tmp/jmeter-$JMETER_VERSION.tgz && \
    rm -f /tmp/jmeter-$JMETER_VERSION.tgz
