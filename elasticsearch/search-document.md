# 데이터 검색

전체 검색

```
GET kibana_sample_data_logs/_search/
{
  "query": {
    "match_all": {}
  }
}
```