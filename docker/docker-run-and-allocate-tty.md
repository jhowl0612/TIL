# 도커 실행과 동시에 내부 접근

```bash
$ docker run -it [이미지명]
$ docker run -it [이미지명] bash
```

`-i` 옵션은 `---interactive`, `-t` 옵션은 `--tty`와 같음

`-i` 옵션은 명령어를 입력받을 수 있도록 하며, `-t` 옵션은 유사 터미널(TTY)을 제공하는 옵션

bash가 기본으로 있지 않은 컨테이너는 bash 커맨드를 추가로 입력하여 bash를 열어야 함