# 검색

```bash
db.[컬렉션명].find({[필드명]:[값]})
db.bios.find({'data.obs_value':860})
db.bios.find({'data.obs_value':860}).skip(100).limit(100)
db.bios.find({'data.obs_item_name_kor':'수온'}).count()
```

`.skip(n)` : 첫 n건 생략

`.limit(n)` : n건만 출력

`.count()` : 검색된 도큐먼트 수 출력