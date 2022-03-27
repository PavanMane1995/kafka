# kafka for windows

Initial kafka setup to kickstart kafka in console

Using kafka version 3.1.0

Make changes in \config\zookeeper.properties and \config\server.properties (Just change the log.dir path)

1)Start zookeeper 
 .\bin\windows\zookeeper-server-start.bat .\config\zookeeper.properties
 
2)Start kafka
 .\bin\windows\kafka-server-start.bat .\config\server.properties

3)Create Topic
 .\bin\windows\kafka-topics.bat --create --topic Student --bootstrap-server localhost:9092
 
4)List the topics
.\bin\windows\kafka-topics.bat --list --bootstrap-server localhost:9092 

4)Run producer
 .\bin\windows\kafka-console-producer.bat --topic Student --bootstrap-server localhost:9092
 
6)Run consumer
 .\bin\windows\kafka-console-consumer.bat --topic Student --bootstrap-server localhost:9092 
