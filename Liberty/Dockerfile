FROM websphere-liberty

MAINTAINER Jamie Coleman <jlcoleman@uk.ibm.com>

COPY server.xml /opt/ibm/wlp/usr/servers/defaultServer/
COPY db2jcc4.jar / 
COPY jdbc_LI_en / 
COPY jdbc_LI_en.rtf / 
COPY 8.0.0.3-WS-MQ-Java-InstallRA.jar / 
COPY MQ_Test.war /opt/ibm/wlp/usr/servers/defaultServer/dropins/
	
RUN installUtility install --acceptLicense defaultServer
RUN java -jar 8.0.0.3-WS-MQ-Java-InstallRA.jar --acceptLicense /
	
ENV LICENSE accept
