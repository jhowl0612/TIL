# 확장 검색

리눅스로 비유하면 파이프라인, SQL에서 으레 GROUP BY 절이 담당하는 기능을 가짐.

```bash
db.search.aggregate([
	{"$group" : { _id : "$data.obs_item_name_kor", count : {$sum : 1 } } },
	{"$sort":{'count ':1} }
])
```

`data.obs_item_name_kor`필드 기준으로 그룹핑

그룹별로 도큐먼트 개수당 +1 = 도큐먼트 수 세기

도큐먼트 수 오름차순(1)정렬. 내림차순은 (-1)