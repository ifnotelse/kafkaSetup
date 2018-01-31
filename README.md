# kafkaSetup

### Step 1: Download the code
 ##### Download the 1.0.0 release and un-tar it.
 > tar -xzf kafka_2.11-1.0.0.tgz
 
 > cd kafka_2.11-1.0.0
 
### Step 2: Start the server
  ##### Zookeeper
  > bin/zookeeper-server-start.sh config/zookeeper.properties
  ##### Kafka-server
  > bin/kafka-server-start.sh config/server.properties
  
### Step 3: Create a topic
 ##### create a topic named "test"
 > bin/kafka-topics.sh --create --zookeeper localhost:2181 --replication-factor 1 --partitions 1 --topic test
 ##### list created  topics
 > bin/kafka-topics.sh --list --zookeeper localhost:2181
### Step 4: Send message
 ##### send some messages for topic test
 > bin/kafka-console-producer.sh --broker-list localhost:9092 --topic test


  
