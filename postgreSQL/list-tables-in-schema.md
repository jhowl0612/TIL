# 특정 스키마 내 테이블 목록 출력


```sql
SELECT * FROM PG_TABLES
WHERE schemaname = '[스키마명(소문자)]'
order by tablename asc ;
```