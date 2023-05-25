# 테이블 덤프

```sql
pg_dump -d [데이터베이스명] -U [유저명] -t [테이블명] > [만들파일명]
/usr/bin/pg_dump -d postgres -U postgres -t arctic_grid > arctic_grid.sql
```