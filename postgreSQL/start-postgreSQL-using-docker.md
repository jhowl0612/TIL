# 도커로 PostgreSQL 시작하기

```bash
$ docker run -d -p 5432:5432 --name pgsql -it --rm -v /home/ubuntu/postgres_data:/var/lib/postgresql/data -e POSTGRES_PASSWORD=[비밀번호] postgres
```
- `-d` : 백그라운드로 실행
- `-p 5432:5432` : 컨테이너 내측 포트 5432와 바깥 5432 연결
- `--name pgsql` : 컨테이너명 pgsql
- `--rm` : 컨테이너 종료 시 자동 삭제
- `-v /home/ubuntu/postgres_data:/var/lib/postgresql/data` : `/home/ubuntu/postgres_data` 디렉토리 만들고 컨테이너 내부의 `/var/lib/postgresql/data` 디렉토리와 연동