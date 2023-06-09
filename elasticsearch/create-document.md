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

수정(POST) 메서드로도 입력할 수 있음
이 경우, 도큐먼트 id를 자동 생성하도록 id를 비워 두고 입력하는 것이 가능
```
POST [인덱스]/_doc {데이터}
```

```
POST disaster_msg/_doc
{
  "timestamp" : "2021-07-24T11:51:36.000",
  "region_cd" : "11010",
  "region_name" : "서울특별시",
  "message" : "[서울특별시]"
}
```
