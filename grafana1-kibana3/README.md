### Get started
1. Pull the docker image: `docker pull fayndee/gsg-elk:grafana1-kibana3`
2. Run the docker container: `docker run -d -p 2003:2003 -p 3000:3000 -p 9200:9200 -p 4560:4560 -p 5601:5601 fayndee/gsg-elk:grafana1-kibana3`

### Built-in service versions

service       | version
------------- | --------
Graphite      | 0.9.x
StatsD        | 0.7.2
Grafana       | 1.9.1
Elasticsearch | 1.4.x
Logstash      | 1.4.x
Kibana        | 3.1.2
