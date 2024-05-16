# logstash-csv-filter-sample
An example demonstrating how to ingest a CSV file into Elasticsearch

# How to
```
docker network create elastic
docker run --name elasticsearch --net elastic --hostname=elasticsearch -p 9200:9200 -it -m 1GB docker.elastic.co/elasticsearch/elasticsearch:8.13.3
docker run --name kibana --net elastic --hostname=kibana -p 5601:5601 docker.elastic.co/kibana/kibana:8.13.3
```
Run logstash:
```
cd /xxx/logstash-8.13.3
bin/logstash -f import-csv.conf
```
