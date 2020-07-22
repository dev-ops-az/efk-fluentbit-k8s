# efk-fluentbit-k8s
# Install and Run elasticsearch  and kibana on docker
docker pull docker.elastic.co/elasticsearch/elasticsearch:7.8.0
docker run --name my_es -p 9200:9200 -p 9300:9300 -e "discovery.type=single-node" docker.elastic.co/elasticsearch/elasticsearch:7.8.0

docker pull docker.elastic.co/kibana/kibana:7.8.0
docker run --name my_kbn --link my_es:elasticsearch -p 5601:5601 docker.elastic.co/kibana/kibana:7.8.0

#install service and fluentbit

cd service-example
...
cd fluentbit
...