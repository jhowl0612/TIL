# 인덱스 매핑

Elasticsearch는 기본적으로 데이터만 입력하면 데이터 타입을 자동으로 정해 주지만 수동으로 명시할(explicit) 수도 있음
```
PUT [인덱스명]
{
  "mappings": {
    "properties": {
      "field1":{"type": "date"},
      "field2":{"type": "integer"}
      ...
    }
  }
}
```

```
PUT covid19-state
{
  "mappings": {
    "properties": {
      "timestamp":{
        "type": "date"
      },
      "geoip" : {
        "properties" : {
          "provinces_code" : {
            "type" : "keyword"
          },
          "municipalities_code" : {
            "type" : "keyword"
          },
          "location" : {
            "type" : "geo_point"
          },
          "provinces_name" : {
            "type" : "keyword"
          },
          "municipalities_name" : {
            "type" : "keyword"
          }
        }
      },
      "message" : {
        "type" : "text",
        "fields" : {
          "keyword" : {
            "type" : "keyword"
          }
        }
      },
      "msg_keyword" : {
        "type" : "text",
        "fields" : {
          "keyword" : {
            "type" : "keyword"
          }
        }
      },
      "count" : {
        "type" : "integer"
      },
      "d7_mean" : {
        "type" : "integer"
      },
      "outlier_area" : {
        "type" : "integer"
      }
    }
  }
}
```