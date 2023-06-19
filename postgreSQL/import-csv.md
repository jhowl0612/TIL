# CSV 데이터 테이블에 삽입

psql 로그인 이후 가능

테이블은 미리 생성해두어야 함

```
copy [테이블명](컬럼1,컬럼2, ...) from '[파일경로]' with delimiter ',';
copy map_water_level(lon,lat,water_level) from '/workspace/soundg_pointz.csv' with delimiter ',';
```