FROM tomcat:8.0-alpine
LABEL maintainer="hyunsangwon93@gmail.com"

RUN rm -rf /usr/local/tomcat/webapps/*
COPY ROOT.war /usr/local/tomcat/webapps/ROOT.war

EXPOSE 8080

CMD ["catalina.sh", "run"]
