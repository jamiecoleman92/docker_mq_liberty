FROM websphere-liberty

MAINTAINER Jamie Coleman <jlcoleman@uk.ibm.com>

COPY server.xml /opt/ibm/wlp/usr/servers/defaultServer/
COPY 8.0.0.3-WS-MQ-Java-InstallRA.jar / 
COPY MQ_Test_2.war /opt/ibm/wlp/usr/servers/defaultServer/dropins/
	
RUN installUtility install --acceptLicense defaultServer
RUN java -jar 8.0.0.3-WS-MQ-Java-InstallRA.jar --acceptLicense /
	
ENV LICENSE accept
