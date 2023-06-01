# 도커로 PostGIS 설치

PostGIS : PostgreSQL의 공간정보 처리 익스텐션

```bash
$ sudo docker run -v [연결할 바깥 디렉토리]:[연결할 컨테이너 내부 디렉토리] -p 5432:5432 -e POSTGRES_PASSWORD=[비밀번호] -d mdillon/postgis
```

기본 스키마로 public, tiger, tiger_data, topology가 생성,

public 스키마에 spatial_ref_sys 테이블이 생성됨