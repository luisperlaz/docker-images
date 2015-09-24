FROM luisperlaz/jmeter-base

#http://jmeter-plugins.org/downloads/file/JMeterPlugins-Standard-1.3.0.zip
ENV JMETER_PLUGINS_VERSION 1.3.0
ENV JMETER_PLUGINS_MIRROR http://jmeter-plugins.org/downloads/file/

ENV JMETER_PLUGINS_STANDARD_DOWNLOAD_URL $JMETER_PLUGINS_MIRROR/JMeterPlugins-Standard-$JMETER_PLUGINS_VERSION.zip
ENV JMETER_PLUGINS_EXTRAS_DOWNLOAD_URL $JMETER_PLUGINS_MIRROR/JMeterPlugins-Extras-$JMETER_PLUGINS_VERSION.zip

MAINTAINER luisperlazaro@gmail.com

VOLUME ["/tests"]
VOLUME ["/data"]
VOLUME ["/logs"]

ADD user.properties $JMETER_HOME/bin/

WORKDIR $JMETER_HOME

ENTRYPOINT [ "bin/jmeter" ]
