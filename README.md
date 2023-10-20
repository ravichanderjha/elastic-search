# elastic-search

## Aggregate
```json
{
  "size": 0,
  "aggs": {
    "group_by_category": {
      "terms": {
        "field": "category.keyword",
        "size": 10  // Number of top categories to return
      }
    }
  }
}
```

In this example:

- `"size": 0` means that you don't want the search results, only the aggregation results.
- `"aggs"` specifies that you want to perform an aggregation.
- `"group_by_category"` is the name of the aggregation.
- `"terms"` specifies that you want to perform a terms aggregation (similar to SQL's GROUP BY).
- `"field": "category.keyword"` specifies the field on which to perform the aggregation. `.keyword` is used for keyword fields to ensure exact matches (without stemming or tokenization).

Make sure to replace `"category.keyword"` with the actual field you want to perform the aggregation on.
