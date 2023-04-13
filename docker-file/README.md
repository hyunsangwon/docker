## Dockerfile 작성법
    파일이름은 Dockerfile 파일 생성시 앞에는 무조건 대문자로 시작  
    확장명을 명시하지 않는다.

### Dockerfile 문법
    Dockerfile은 다음과 같은 INSTRUCTIONs를 사용
- FROM: 기본 이미지를 지정합니다.
- RUN: 명령어를 실행하여 이미지를 빌드합니다.
- CMD: 컨테이너가 실행될 때 실행될 기본 명령을 지정합니다.
- COPY: 파일을 복사합니다.
- ADD: 파일을 복사하거나 URL에서 파일을 다운로드하고 압축을 풉니다.
- WORKDIR: 명령이 실행될 디렉토리를 설정합니다.
- EXPOSE: 컨테이너가 사용하는 포트를 지정합니다.
- ENV: 환경 변수를 설정합니다.
- ARG: 빌드 중에 사용할 인수를 정의합니다.
- ENTRYPOINT: 컨테이너가 시작될 때 실행될 명령을 지정합니다.
- VOLUME: 볼륨을 지정합니다.

### 주의사항
 컨테이너는 대부분은 최소화를 중요시. 딱 필요한 것만 설치

### Example
```dockerfile
FROM nginx:latest

WORKDIR /usr/share/nginx/html
COPY index.html index.html

EXPOSE 80

CMD ["nginx", "-g", "daemon off;"]
```
 nginx:latest 이미지를 기본 이미지로 사용하고, 작업 디렉토리를 /usr/share/nginx/html로 설정하고, index.html 파일을 해당 디렉토리로 복사하며, 80 포트를 노출하고, 컨테이너가 시작될 때 nginx를 실행.
