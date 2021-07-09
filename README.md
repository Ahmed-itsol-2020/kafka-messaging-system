##SETUP 
```
docker run -d  --net=host --name=zookeeper -e ZOOKEEPER_CLIENT_PORT=32181 -e ZOOKEEPER_TICK_TIME=2000 -e ZOOKEEPER_TICK_TIME=2000 confluentinc/cp-zookeeper
```

```
docker run -d --net=host --name=kafka -e KAFKA_ZOOKEEPER_CONNECT=localhost:32181 -e KAFKA_ADVERTISED_LISTENERS=PLAINTEXT://localhost:29092 -e KAFKA_BROKER_ID=2 -e KAFKA_OFFSETS_TOPIC_REPLICATION_FACTOR=1 confluentinc/cp-kafka
```