# Docker GSG/ELK Image
Docker image of metrics (Graphite, StatsD, Grafana) and logs (Elasticsearch, Logstash, Kibana) monitoring tools bundle.
This image is based on [Kamon Grafana Graphite](https://github.com/kamon-io/docker-grafana-graphite) docker image.

### Tags
- grafana1-kibana3: grafana 1.x.x & kibana 3.x.x
- grafana1-kibana4: grafana 1.x.x & kibana 4.x.x

### Get started

1. Pull the docker image: `docker pull fayndee/gsg-elk:TAG`
2. Run the docker container: `docker run -d -p 2003:2003 -p 3000:3000 -p 9200:9200 -p 4560:4560 -p 5601:5601 fayndee/gsg-elk:TAG`

### Ports configuration

Service ports are configured as below and are exposed by default.

port | protocol | service       | description
---- | -------- | ------------- | ------------------------------------------
2002 | UDP      | Carbon Cache  | Carbon Cache UDP input port.
2003 | TCP      | Carbon Cache  | Carbon Cache line (plain text) input port.
2004 | TCP      | Carbon Cache  | Carbon Cache pickle input port.  
8000 | TCP      | Graphite Web  | Graphite Web UI port.
8125 | UDP      | StatsD        | StatsD UDP input port.
8126 | TCP      | StatsD        | StatsD management port.
3000 | TCP      | Grafana       | Grafana UI port.
9200 | TCP      | Elasticsearch | Elasticsearch service port.
4560 | TCP      | Logstash      | Logstash TCP JSON input port.
4570 | UDP      | Logstash      | Logstash UDP JSON input port.
5601 | TCP      | Kibana        | Kibana UI port.
