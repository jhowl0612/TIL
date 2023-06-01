# PostgreSQL client 설치

클라이언트 설치 시 도커로 PSQL을 설치했더라도 컨테이너 진입 명령 없이 psql 로그인 가능
```bash
$ sudo apt-get install curl ca-certificates gnupg
$ curl https://www.postgresql.org/media/keys/ACCC4CF8.asc | sudo apt-key add -
$ sudo sh -c 'echo "deb http://apt.postgresql.org/pub/repos/apt $(lsb_release -cs)-pgdg main" > /etc/apt/sources.list.d/pgdg.list'
$ sudo apt-get update
$ sudo apt install postgresql-client-11
$ pg_basebackup -V
```