# Oracle DB 연결

```bash
pip install cx_Oracle
```

파이썬 스크립트에서 import

```python
import cx_Oracle as co
```

연결 구문 작성 

```python
conn = co.connect('ID/PW@192.168.nnn.nnn:5432/xe')    
                # 아이디/비밀번호@호스트:포트/xe     
```

기초적인 쿼리 실행법

```python
cursor = conn.cursor()
query = """ 실행할 쿼리문 """
cursor.execute(query)
```

