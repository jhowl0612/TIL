# Elasticsearch 연결

```bash
pip install elasticsearch
```

이후 파이썬 스크립트에서 import

```python
from elasticsearch import Elasticsearch
```

연결 구문 작성 

```python
es = Elasticsearch(
['주소:포트'], # 호스트, 기본 포트는 9200
http_auth = ('유저명', '비밀번호')
)                   
```

기초적인 쿼리 실행법

```python
query = """ 실행할 쿼리문 """
es.search(query)
```

