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

_bulk 사용하여 한 번에 여러 도큐먼트 입력 가능

```
POST [인덱스]/_bulk
{"index":{"_id":"1"}}
{데이터}
{"index":{"_id":"2"}}
{데이터}
{"index":{"_id":"3"}}
{데이터}
...
```

```
POST /my_index/_bulk
{"index":{"_id":"1"}}
{"timestamp":"2021-07-27T12:04:15+09:00", "geoip" : { "provinces_code" : "KR-41", "municipalities_code" : "31014", "provinces_name": "경기도", "region_name" : "수원시영통구", "location" : { "lon" : 127.0, "lat" : 37.3 } }, "message":"메시지 전문", "msg_keyword":"볼링장"}
{"index":{"_id":"2"}}
{"timestamp":"2021-07-27T12:36:15+09:00", "geoip" : { "provinces_code" : "KR-41", "municipalities_code" : "31014", "provinces_name": "경기도", "region_name" : "수원시영통구", "location" : { "lon" : 127.0, "lat" : 37.3 } }, "message":"메시지 전문", "msg_keyword":"수원시청"}
```
