# Kafka Zookeeper
|Command| Description|
|-------|------------|
|`bin/zookeeper-server-start.sh config/zookeeper.properties`|Starts zookeeper|
|`bin/zookeeper-server-stop.sh config/zookeeper.properties`|Stops zookeeper|

# Kafka Server
|Command| Description|
|-------|------------|
|`bin/kafka-server-start.sh config\server.properties`|Starts kafka server|
|`bin/kafka-server-stop.sh config\server.properties`|Stops kafka server|

# Kafka Topic
|Command| Description|
|-------|------------|
|`bin/kafka-topics.sh --create --bootstrap-server localhost:9092 --replication-factor 1 --partitions 1 --topic test`|Creates topic|
|`bin/kafka-topics.sh --list --bootstrap-server localhost:9092`|Lists topics|
