. Apache Kafka was originated at LinkedIn and later became an open sourced Apache project in 2011.
. Kafka is a distributed messaging system.

. Messaging system:
  1) Point-to-point :

          m1                   m1
  sender ----> Message_Queue ----> Receiver

  2) Pub-Sub (Publish-Subscribe):
                                 m1
                             -----------> Receiver
                             |
          m1                 |   m1
  Sender -----> Topic ------------------> Receiver
                             |
                             |   m1
                             -----------> Receiver

. Control zookeeper bin/zkServer.sh status/start/stop
  Connect to zk: bin/zkCli.sh

. Control zookeeper from kafka directory
  bin/zookeeper-server-start.sh config/zookeeper.properties &
  bin/zookeeper-server-stop.sh config/zookeeper.properties &

  Add & at the end to run service int he background

  Check Status by `ps -ef | grep "zookeeper"`

. Control Kafka
  bin/kafka-server-start.sh config/server.properties &
  bin/kafka-server-stop.sh config/server.properties &

  verify :
  ps -ef | grep "kafka"

  Output will contain two process running one is zookeeper and other one is kafka

  Commands:
  Start the Zookeeper : bin/zookeeper-server-start.sh config/zookeeper.properties
  Start the Kafka server : bin/kafka-server-start.sh config/server.properties
  Create a topic  "test" : bin/kafka-topics.sh --create --zookeeper localhost:2181 --replication-factor 1 --partitions 1 --topic test
  List topic command :
  bin/kafka-topics.sh --list --zookeeper localhost:2181 test

.  jps
    31700 Kafka
    1318 Jps
    31517 QuorumPeerMain    <This is zookeeper cluster name>

.  Create topics
   Syntax

    bin/kafka-topics.sh --create --zookeeper localhost:2181 --replication-factor 1
    --partitions 1 --topic topic-name
    Example

    bin/kafka-topics.sh --create --zookeeper localhost:2181 --replication-factor 1   
    --partitions 1 --topic Hello-Kafka
.   List topics
    bin/kafka-topics.sh --list --zookeeper localhost:2181

.   partitions and replication-factor can only be increased not decreased.
