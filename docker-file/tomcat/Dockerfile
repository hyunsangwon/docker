FROM centos
LABEL maintainer="hyunsangwon93@gmail.com"

RUN mkdir /opt/tomcat/

WORKDIR /opt/tomcat
RUN curl -O https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.6/bin/apache-tomcat-9.0.6.tar.gz
RUN tar xvf apache-tomcat-9.0.6.tar.gz
RUN mv apache-tomcat-9.0.6/* /opt/tomcat/.
RUN yum install java-1.8.0-openjdk-devel.x86_64 -y
RUN java -version

WORKDIR /opt/tomcat/webapps
RUN curl -O -L https://github.com/HyunSangWon/docker/blob/master/docker-file-practice02/ROOT.war

EXPOSE 8080

CMD ["/opt/tomcat/bin/catalina.sh", "run"]
