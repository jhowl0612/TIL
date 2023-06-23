# PostGIS에 shp2pgsql로 shp 업로드

PostGIS : PostgreSQL의 공간정보 처리 익스텐션

```bash
shp2pgsql -s [좌표계] -W cp949 [shp 파일경로] | psql -U [유저명] -d [데이터베이스명]
shp2pgsql -s 4326 -W cp949 grid.shp | psql -U postgres -d postgres
```

- `-s` 필수옵션. shp 파일의 좌표계
- `-W` 한글 있을 경우 필요. 인코딩

