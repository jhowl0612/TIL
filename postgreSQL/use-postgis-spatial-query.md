# PostGIS 공간쿼리 사용

PostGIS : PostgreSQL의 공간정보 처리 익스텐션

```sql
select *, st_distance(geom, ST_SetSRID(ST_POINT(cast([위도] as double precision ),  cast([경도] as double precision )), [좌표계])) as d from [테이블명];

select *, st_distance(geom, ST_SetSRID(ST_POINT(cast(35.1 as double precision ),  cast(135.5 as double precision )), 4326)) as d from obs order by d limit 1;
```

테이블 row 전체, 거기에 더해 각 row의 geom(geometry 타입) 필드와 특정 위경도와의 거리 출력

거리(as d) 순으로 정렬, 첫 번째만 출력

