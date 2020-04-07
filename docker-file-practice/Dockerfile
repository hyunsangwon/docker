FROM tomcat:8.0-alpine
LABEL maintainer="hyunsangwon93@gmail.com"

WORKDIR /usr/local/tomcat/webapps/
RUN curl -O -L https://github.com/HyunSangWon/docker/blob/master/docker-file-practice/ROOT.war

EXPOSE 8080

CMD ["catalina.sh", "run"]