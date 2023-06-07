# 데이터 입력

특정 도큐먼트 id에 데이터 입력

```
PUT [인덱스]/_doc/[도큐먼트 id] {데이터}
```

```
PUT disaster_msg/_doc/1
{
  "timestamp" : "2021-07-24T11:51:36.000",
  "region_cd" : "11010",
  "region_name" : "서울특별시",
  "message" : "[서울특별시]"
}
```