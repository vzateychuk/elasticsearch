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
