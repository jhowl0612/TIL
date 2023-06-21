# CSV로 테이블 데이터 내보내기

psql 로그인 이후 가능
excel 이 읽을 수 있는 인코딩은 EUC-KR
```
copy (select * from [테이블명]) To '[파일경로]' with csv DELIMITER ',' ENCODING 'EUC-KR';
copy (select * from map_info) To '/var/lib/postgresql/data' with csv DELIMITER ',' ENCODING 'EUC-KR';
```