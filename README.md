# elasticsearch
Practicing with elastic search + kibana. Based on https://www.linkedin.com/learning/elasticsearch-essential-training

# Run elastic search with Kibana
```shell
docker-compose up -d
```

## Open browser
```
http://localhost:5601/app/dev_tools#/console
```

## Data manipulation commands

<REST-Verb> <Index> <Type> <ID>

Examples:
---

Upsert new document
```
PUT sales order 123
```

Get document by ID
```
GET sales order 123
```

Delete entire index
```
DELETE sales
```

## Cluster health
```
GET /_cat/health
```

## Nodes
```
GET /_cat/nodes
```

## Indexes
```
GET _cat/indices
```

## Bulk load
```
POST _bulk
{ "index" : { "_index" : "my-test", "_type" : "my-type", "_id" : "1" } }
{ "col1" : "val1"}
{ "index" : { "_index" : "my-test", "_type" : "my-type", "_id" : "2" } }
{ "col1" : "val2"}
{ "index" : { "_index" : "my-test", "_type" : "my-type", "_id" : "3" } }
{ "col1" : "val3" }

GET /my-test

GET /my-test/my-type/1
```

### Bulk load from file
```shell
curl -s -H "Content-Type: application/x-ndjson" -XPOST localhost:9200/_bulk --data-binary "@reqs"; echo
```
where _reqs_ if file name with data