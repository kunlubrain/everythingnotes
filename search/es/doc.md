/show indices
curl http://localhost:9200/_aliases
curl http://localhost:9200/_aliases?pretty=true

/delete one index
curl -s -XDELETE 'http://localhost:9200/myindex'

/create a new index using mapping
curl -s -XPUT 'http://localhost:9200/myindex' --data-binary '@myindex_mapping.json' -H 'Content-Type: application/json'
