# 도커로 몽고DB 시작하기

```bash
$  docker run --rm --name mongodb -p 27017:27017 -e MONGO_INITDB_ROOT_USERNAME=[유저명설정] -e MONGO_INITDB_ROOT_PASSWORD=[비밀번호설정] -v ~/mongo_db_files:/data/db -d mongo:4.4.6
```
- `--rm` : 컨테이너 종료 시 자동 삭제
- `--name mongodb` : 컨테이너명 mongodb
- `-p 27017:27017` : 컨테이너 내측 포트 27017과 바깥 27017 연결
- `-v ~/mongo_db_files:/data/db` : 현위치에 `mongo_db_files`이름의 디렉토리 만들고 컨테이너 내부의 `/data/db` 디렉토리와 연동
- `-d mongo:4.4.6` : mongo 이미지 버전 4.4.6