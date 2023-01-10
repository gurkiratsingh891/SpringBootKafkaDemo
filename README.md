# SpringBootKafkaDemo
-Sample Spring Boot application with Rest API which receives message from user and publishes to kafka topic
-Then these messages are received by the Kafka listner/consumer which is created in the application
-Covers simple string message and json message.

Steps to setup Kafka
For windows only

	1. Start the zookeeper service
.\bin\windows\zookeeper-server-start.bat .\config\zookeeper.properties 

	2. Run the kafka server
	
	.\bin\windows\kafka-server-start.bat .\config\server.properties
	
	Check whether kafka runs on port 9092
	
	3. Create a kafka topic
	.\bin\windows\kafka-topics.bat --create --topic topic-example --bootstrap-server localhost:9092

	4. Adding messages to the topic (using the producer)
	.\bin\windows\kafka-console-producer.bat --topic topic-example --bootstrap-server localhost:9092
	Type the messages in the arrow sign
	>helloworld
	>demo

	5. Consuming/reading the events from kafka
.\bin\windows\kafka-console-consumer.bat --topic topic-example --from-beginning --bootstrap-server localhost:9092![image](https://user-images.githubusercontent.com/47685401/211437284-a45bd809-65e8-4e7c-aa1b-37661f20db60.png)
