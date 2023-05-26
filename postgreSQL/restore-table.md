# 테이블 리스토어

sql
```sql
psql -d [데이터베이스명] -U [유저명] -f [읽어올 파일]
psql -U postgres -d postgres -f arctic_grid.sql
```

csv (테이블 미리 생성 필요)
```sql
copy 테이블명(컬럼1,컬럼2,컬럼3...) from '[파일경로]' with delimiter ',';
copy map_water_level(lon,lat,water_level) from '/soundg_pointz.sql' with delimiter ',';
```