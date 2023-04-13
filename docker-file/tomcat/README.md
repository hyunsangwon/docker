## Getting started
    1. git clone https://github.com/HyunSangWon/docker.git  
    2. cd docker/docker-file-practice02
    3. ls
    4. docker build -t sangwondocker/tomcat8 . (dockerfile 이미지로 빌드)  
    5. docker image ls (전체 이미지 확인)
    6. docker container run -it -d --name tomcatcontainer -p 80:8080 sangwondocker/tomcat8 (이미지를 백그라운드로 실행)  
    7. docker ps  or docker container ls (실행중인 도커컨테이너 확인)

## 이미지 배포하기
    1. docker login  
    2. docker push sangwondocker/tomcat8  