# 도커 밖에서 안으로 파일 넣기

```bash
$ docker cp [파일경로] [컨테이너명]:[컨테이너 내 경로]
$ docker cp /etc/file.csv 53f9:/etc
```

안에서 밖으로도 가능
