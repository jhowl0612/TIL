# PostgreSQL DB 연결

```bash
sudo apt update
sudo apt install libpq-dev python-dev postgresql postgresql-contrib
pip3 install psycopg2
```

psycopg2가 필요로 하는 패키지들을 먼저 설치해야 함

이후 파이썬 스크립트에서 import

```python
import psycopg2 as pg2 
```

연결 구문 작성 

```python
conn = pg2.connect(database="DB명", 
user="유저명",
password="비밀번호",
host="IP",
port="5432")
```

기초적인 쿼리 실행법

```python
cur = conn.cursor() 
query = """ 실행할 쿼리문 """
cur.execute(query)
```

