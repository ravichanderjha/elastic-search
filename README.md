# elastic-search

## Aggregate
### Count 
{
  "size": 0,
  "aggs": {
    "status_count": {
      "terms": {
        "field": "status.keyword",
        "size": 10  // Number of top status values to return
      }
    }
  }
}
