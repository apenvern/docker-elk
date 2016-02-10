# docker-elk
ELK Stack on docker with docker-compose

## How to start

```
# Clone the repository
git clone https://github.com/apenvern/docker-elk.git
# Start the container with Docker compose
docker-compose up -d 
```

## How to test
```
# Inject logs
docker run --rm --log-driver=gelf --log-opt gelf-address=udp://localhost:12201 --link logstash:logstash --name log_gen debian:jessie bash -c 'for i in {0..2000}; do echo "Hello World "$i; done'
```

Elasticsearch URL : http://*hostname*:9200/

Kibana URL :  http://*hostname*:5601/app/kibana
