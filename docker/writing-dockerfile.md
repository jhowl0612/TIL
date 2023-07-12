# 도커파일 작성

```dockerfile
FROM ubuntu:bionic
# 사용할 OS 이미지 가져오기

RUN apt update
RUN apt-get install -y default-jre
# 커맨드 실행
# 중간에 Y/N? 물어보면 대답을 기다리며 멈춰버리므로 -y 옵션

ADD apache-tomcat-8.5.69.tar.gz /tomcat
# COPY는 압축해제 없이, ADD는 압축해제해서 추가하는 명령

COPY entrypoint.sh /bin/
RUN chmod 775 /bin/entrypoint.sh

EXPOSE 8080
# 8080 포트를 외부에 개방

WORKDIR /bin
# 이미지를 컨테이너로 실행할 때 시작 위치 정하는 명령

CMD ["./entrypoint.sh"]
# CMD라는 명령은 단 한번밖에 쓸 수 없으므로, 셸을 실행시킴
# 이름은 상관없지만 관습적으로 entrypoint.sh
```
