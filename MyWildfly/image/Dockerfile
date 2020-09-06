FROM jboss/wildfly
WORKDIR /opt/jboss/wildfly/modules/system/layers/base/com/
RUN mkdir mysql
WORKDIR mysql/
RUN mkdir main
WORKDIR /opt/jboss/wildfly/
CMD ["/opt/jboss/wildfly/bin/standalone.sh", "-b", "0.0.0.0", "-bmanagement", "0.0.0.0"]
