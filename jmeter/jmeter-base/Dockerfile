FROM ubuntu:14.04

MAINTAINER luisperlazaro@gmail.com

ENV JDK_PACKAGE openjdk-7-jdk
ENV JMETER_VERSION 2.13
ENV JMETER_MIRROR http://www.eu.apache.org/dist/jmeter/binaries/
ENV JMETER_DOWNLOAD_URL $JMETER_MIRROR/apache-jmeter-$JMETER_VERSION.tgz
ENV BASE_DIR /var/lib
ENV JMETER_HOME $BASE_DIR/apache-jmeter-$JMETER_VERSION

ENV JMETER_PLUGINS_VERSION 1.3.0
ENV JMETER_PLUGINS_MIRROR http://jmeter-plugins.org/downloads/file/
ENV JMETER_PLUGINS_STANDARD_DOWNLOAD_URL $JMETER_PLUGINS_MIRROR/JMeterPlugins-Standard-$JMETER_PLUGINS_VERSION.zip
ENV JMETER_PLUGINS_EXTRAS_DOWNLOAD_URL $JMETER_PLUGINS_MIRROR/JMeterPlugins-Extras-$JMETER_PLUGINS_VERSION.zip

RUN \
    apt-get update && \
    apt-get -y install $JDK_PACKAGE curl unzip

# Install jmeter
RUN curl $JMETER_DOWNLOAD_URL -o /tmp/jmeter-$JMETER_VERSION.tgz && \
    cd $BASE_DIR && tar xf /tmp/jmeter-$JMETER_VERSION.tgz && \
    rm -f /tmp/jmeter-$JMETER_VERSION.tgz

# Install jmeter standard plugins
RUN curl $JMETER_PLUGINS_STANDARD_DOWNLOAD_URL -L -o /tmp/jmeter-plugins-standard.zip && \
    cd $JMETER_HOME && unzip -o /tmp/jmeter-plugins-standard.zip && \
    rm -f /tmp/jmeter-plugins-standard.zip

# Install jmeter extra plugins
RUN curl $JMETER_PLUGINS_EXTRAS_DOWNLOAD_URL -L -o /tmp/jmeter-plugins-extras.zip && \
    cd $JMETER_HOME && unzip -o /tmp/jmeter-plugins-extras.zip && \
    rm -f /tmp/jmeter-plugins-extras.zip
