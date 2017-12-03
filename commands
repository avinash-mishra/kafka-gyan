## Basic commands

* Start Zookeeper

> bin/zookeeper-server-start.sh config/zookeeper.properties

* Start Kafka

> bin/kafka-server-start.sh config/server.properties

* Creating Kafka topic

> bin/kafka-topics.sh --create --zookeeper localhost:2181 --replication-factor 1
--partitions 1 --topic topic-namr

* List Kafka topic

> bin/kafka-topics.sh --list --zookeeper localhost:2181

* Start producer to send message

> bin/kafka-console-producer.sh --broker-list localhost:9092 --topic topic-name

* Start consumer to consume messages

> bin/kafka-console-consumer.sh --zookeeper localhost:2181 —topic topic-name
--from-beginning

* Delete kafka topics

> bin/kafka-topics.sh --zookeeper localhost:2181 --delete --topic topic_name
