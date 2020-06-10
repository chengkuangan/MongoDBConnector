# Kafka MongoDB Connector

1. Create the necessary Dockerfile as per the following.
```
FROM registry.redhat.io/amq7/amq-streams-kafka-23:1.3.0
USER root:root
COPY ./mongo-plugins/ /opt/kafka/plugins/
USER kafka:kafka
```

2. Create a folder named `mongo-plugins` under the project root folder.

2. Download the MongoDB Kafka Connect zip file from from 
[MongoDB website](https://www.mongodb.com/kafka-connector). Unzip the zip file and copy the .jar file from the unzip `lib` folder to the `mongo-plugins` folder.

3. Build the docker image from the project root folder using the following command:
```
docker image build
```

