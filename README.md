## 개요
 도커 개념과 Dockerfile 작성법을 알아보자 

## 도커란?
    컨테이너 기반 가상화 플랫폼.
    소프트웨어를 패키징하고 배포하는데 매우 유용
 
### 컨테이너란?
 리눅스 컨테이너는 운영체제 수준의 가상화 기술로 리눅스 커널을 공유하면서 프로세스를 격리된 환경에서 실행하는 기술을 의미  
 하드웨어를 가상화하는 가상 머신과 달리 커널을 공유하는 방식이기 때문에 실행 속도가 빠르고, 성능 상의 손실이 거의 없다는 장점  

### 도커 이미지와 컨테이너
 이미지는 실행파일, 컨테이너는 프로세스  

### 도커를 사용하는 이유

1. 환경 일관성 유지
    * 운영하면서 만들어지는 Snowflake Servers를 방지
    * 모든 환경에서 일관된 동작을 보장
2. 리소스 효율성
    * 도커는 가상머신과 달리 게스트 운영 체제를 각각 설치하지 않아도 되기 때문에 호스트 운영 체제와 자원을 공유
3. 이식성
    * 도커를 사용하면 애플리케이션을 패키징하여 어디서든 실행할 수 있습니다. 이는 다양한 운영 체제와 클라우드 플랫폼에서 실행할 수 있다는 것을 의미

## Dockerfile (파일에 자체 DSL Domain-specific language) 
 Docker Image를 생성하기 위해 명령어로 작성된 문서  
 Container 내부 환경을 정의함  
 Dockerfile을 사용하면 서버 운영 기록을 코드로 관리할 수 있다

## Docker download on CentOS
 1. yum -y update
 2. yum -y install docker docker-registry  
 (docker-registry 는 도커 이미지를 공유하기 위한 서버 애플리케이션)
 3. systemctl enable docker.service  
 4. systemctl start docker.service  

## 자주 사용하는 Docker 문법
 - docker image ls (실행중인 도커 이미지 확인)  
 - docker run -it -d --name tomcatcontainer -p 80:8080 sangwondocker/tomcat8 (컨테이너 백그라운드로 실행)  
 - docker build -t [Name Of the Image]  . (Dockerfile 배포)  
 - docker rm [container id] (컨테이너 삭제)  
 - docker rmi [image id] (이미지 삭제)  
 - docker ps (실행중인 컨테이너 확인)  
 - docker container exec -it [container id] /bin/sh (컨테이너로 접속)
 - docker restart [컨테이너 아이디] (컨테이너 재시작)  

## 트러블슈팅
 - 도커 컨테이너를 재시작하게 되면 기존 로그는 날라간다. 어떻게 로그를 관리할지?  
 => answer : volume 옵션을 사용하자  
 - Dockerfile 배포를 어떻게 하면 더 쉽게 할지...  
