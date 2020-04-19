## 도커컴포즈 란?
컨테이너를 구동시키려면 장황한 명령어를 입력해야하는 불편함과  
컨테이너 간 실행 순서나 의존성을 관리할 수 있는 설정 파일  
컨테이너 실행에 필요한 옵션을 docker-compose.yml 파일에 적어 두면된다.  

## 주의사항
도커 엔진 버전이 1.13.1, 도커 컴포즈 버전은 1.6.0 이상이어야 한다.  
최근에 설치 했다면 문제 없다.  

## docker-composr 다운로드  
- sudo curl -L "https://github.com/docker/compose/releases/download/1.25.5/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose  
- sudo chmod +x /usr/local/bin/docker-compose  

## docker-compose.yml 파일
version: '3' 파일의 첫 줄에는 파일 규격 버전을 적는다. 파일의 규격에 따라
지원하는 옵션이 달라지는데, "3"은 3버전을 사용한다는 의미다.  

service: 실행하려는 컨테이너들을 정의한다. 1개의 서비스에 여러 컨테이너가 있는 개념이다.  

context: docker build 명령을 실행할 디렉터리 경로  
