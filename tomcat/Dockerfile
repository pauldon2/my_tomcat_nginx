FROM tomcat:alpine


ADD users.xml /usr/local/tomcat/conf/tomcat-users.xml
ADD context.xml /usr/local/tomcat/webapps/manager/META-INF/context.xml

ADD sample.war /usr/local/tomcat/webapps/

EXPOSE 8080

WORKDIR /usr/local/tomcat

