# 스키마 목록 출력

DB내 스키마 목록 이름순 출력


```sql
select nspname from pg_catalog.pg_namespace order by nspname;
```