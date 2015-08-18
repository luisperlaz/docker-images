FROM luisperlaz/jmeter-base

MAINTAINER luisperlazaro@gmail.com

VOLUME ["/tests"]
VOLUME ["/data"]
VOLUME ["/logs"]

ADD user.properties $JMETER_HOME/bin/

WORKDIR $JMETER_HOME

ENTRYPOINT [ "bin/jmeter" ]
