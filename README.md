# Docker GSG/ELK Image
Docker image of metrics (Graphite, StatsD, Grafana) and logs (Elasticsearch, Logstash, Kibana) monitoring tools bundle. 

### Get started

1. Pull the docker image: `docker pull fayndee/gsg-elk`
2. Run the docker container: `docker run -d -p 8125:8125/udp -p 8080:8080 -p 4570:4570/udp -p 5601:5601 fayndee/gsg-elk`

### Ports configuration

Service ports are configured as below and are exposed by default.

port | protocol | service       | description
---- | -------- | ------------- | -----------------------------------
2003 | TCP      | Carbon Cache  | Graphite Carbon Cache service port.  
8000 | TCP      | Graphite Web  | Graphite Web UI port.
8125 | UDP      | StatsD        | StatsD UDP input port.
8126 | TCP      | StatsD        | StatsD management port.
8080 | TCP      | Grafana       | Grafana UI port.
9200 | TCP      | Elasticsearch | Elasticsearch service port.
4560 | TCP      | Logstash      | Logstash TCP JSON input port.
4570 | UDP      | Logstash      | Logstash UDP JSON input port.
5601 | TCP      | Kibana        | Kibana UI port.
