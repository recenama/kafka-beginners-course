# kafka-beginners-course

## Run locally
- Download Apache kafka from official site [here](https://kafka.apache.org/downloads)
- Install Apache kafka, you can follow the steps [How to Install Apache Kafka on Mac?](https://www.conduktor.io/kafka/how-to-install-apache-kafka-on-mac/)
- Start Zookeeper ```zookeeper-server-start.sh ~/kafka_2.13-3.7.0/config/zookeeper.properties```
- Start Apache Kafka ```kafka-server-start.sh ~/kafka_2.13-3.7.0/config/server.properties```
- Create a topic```kafka-topics.sh --create --bootstrap-server localhost:9092 --replication-factor 1 --partitions 3 --topic <TOPIC_NAME>```
### Useful Commands for CLI
```
  kafka-topics.sh --list --bootstrap-server localhost:9092
  kafka-topics.sh --describe --bootstrap-server localhost:9092 --topic <TOPIC_NAME>
  kafka-topics.sh --bootstrap-server localhost:9092 --delete --topic <TOPIC_NAME>
  kafka-console-consumer.sh --bootstrap-server localhost:9092 --topic <TOPIC_NAME> --from-beginning
```

### Important notes about Kafka 3(version used here)
Properties by default
```
  enable.idempotence = true
  acks = -1
  retries = 2147483647
```
