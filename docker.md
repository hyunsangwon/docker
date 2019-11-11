## Hello Docker!
![Alternative String](https://subicura.com/assets/article_images/2017-01-19-docker-guide-for-beginners-1/docker-logo.png "Docker")

### What is Docker ?

리눅스의 컨테이너 기술을 기반으로 만든 프로그램.
**컨테이너는 쉽게 말해 애플리케이션 환경에 구애 받지 않고 실행하는 기술**
가상머신과 다르게 프로세스를 격리만 할뿐 운영체제를 뛰우지 않는 프로그램

### When do i use docker?

도커없이 배포/운영 하는데 있어 무리가 없다면 사용안해도 된다.
하지만 서버가 늘어 날 수록 각 개발환경이 어느덧 달라지게 구성이 된다.
이렇게 서로 모양이 다른 서버들이 존재하는 상황을 Snowflakes Server(눈송이 서버) 라고 한다.
Snowflakes Server가 점점 커지면 관리하기가 매우 어렵게 되며 서버마다 배포 환경이 다르기에
개발자도 애를 먹는다. 즉, **Snowflakes Server가 커지기 전에 모든 서버의 환경을 동일하게 맞출때 사용하면 적절하겠다.**

### Docker image and container

이미지는 *실행파일*
컨테이너는 *프로세스*

### How to use docker properly?

a. Docker 컨테이너에서 실행되는 어플리케이션은 back ground모드가 아닌 fore ground 모드로 
실행해야 한다. 서비스 런칭전 에는 back ground로 하다 운영시 fore ground로 유동적이게

b. Docker container 를 이용하여 apache 를 지속적으로 실행하고 서비스 하고 싶다면 apache 를 foreground 로,
docker container 를 background 로 실행하고 exec 를 통하여 container 에 접속하면 된다.

c. Docker 컨테이너는 대부분은 최소화를 중요시. 딱 필요한 것만 설치