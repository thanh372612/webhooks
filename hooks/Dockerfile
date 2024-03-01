FROM jboss/jbpm-server-full:7.61.0.Final
RUN mkdir -p /opt/jboss/wildfly/hooks
COPY ./git-push-2.1-SNAPSHOT.jar /opt/jboss/wildfly/hooks/
COPY ./post-commit /opt/jboss/wildfly/hooks/
COPY ./standalone.xml /opt/jboss/wildfly/standalone/configuration
WORKDIR /opt/jboss/wildfly/bin/
CMD ["./start_jbpm-wb.sh"]