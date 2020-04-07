# Dockerfile :whale:

## Dockerfile 작성법
 파일이름은 Dockerfile 파일 생성시 앞에는 무조건 대문자로 시작  
 확장명을 명시하지 않는다.

## Getting started
    1. git clone https://github.com/HyunSangWon/docker.git  
    2. cd docker/docker-file-practice
    3. ls
    4. docker build -t sangwondocker/tomcat8 .
    5. docker image ls
    6. docker container run -it -d --name tomcatcontainer -p 80:8080 sangwondocker/tomcat8
    7. docker ps