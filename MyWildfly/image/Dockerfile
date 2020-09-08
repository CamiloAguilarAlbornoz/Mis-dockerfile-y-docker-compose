FROM jboss/wildfly:latest
WORKDIR /opt/jboss/wildfly/modules/system/layers/base/com/
RUN mkdir mysql
WORKDIR mysql/
RUN mkdir main
WORKDIR /opt/jboss/wildfly/

# Appserver

ENV WILDFLY_USER Camilo
ENV WILDFLY_PASS kagx25pass

# Database

ENV DB_NAME prueba
ENV DB_USER Camilo
ENV DB_PASS kagx25pass
ENV DB_URI db:3306

ENV MYSQL_VERSION 8.0.21
ENV JBOSS_CLI /opt/jboss/wildfly/bin/jboss-cli.sh
ENV DEPLOYMENT_DIR /opt/jboss/wildfly/standalone/deployments/

# Setting up WildFly Admin Console
RUN echo "=> Adding WildFly administrator"
RUN /opt/jboss/wildfly/bin/add-user.sh Camilo kagx25pass --silent

EXPOSE 8080 9990 8009
CMD ["/opt/jboss/wildfly/bin/standalone.sh", "-b", "0.0.0.0", "-bmanagement", "0.0.0.0"]
