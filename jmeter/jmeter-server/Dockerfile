FROM luisperlaz/jmeter-base

MAINTAINER luisperlazaro@gmail.com

VOLUME [ "/logs" ]
VOLUME [ "/data" ]

ADD user.properties $JMETER_HOME/bin/

# Expose jmeter-server's port (values dicated by those specified in jmeter.properties.
EXPOSE 1099 4000

WORKDIR $JMETER_HOME

# Run jmeter-server 
ENTRYPOINT [ "bin/jmeter-server" ]

