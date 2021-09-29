# Developing Performant Kafka Applications
Workshop for Big Data Conference 2021

## Requirements

For this workshop it is required to have Docker and Docker compose installed in your computer. Follow the instructions [here](https://docs.docker.com/compose/install/)

JDK (at least version 8) has to be installed.

## Instructions

Once Docker and Compose are installed, run the following command:

```shell
./gradlew :requirements:kafkacli
./gradlew :requirements:docker
```

Go to ```requirements/docker``` folder and edit the file docker-compose.yml. Change the value of the variable ```KAFKA_ADVERTISED_HOST_NAME``` to your computer's ip and then save the file.

DO NOT use the ip 127.0.0.1, some exercises won't work if you use that ip.

Finally start the containers by typing:

```shell
docker-compose up -d
```

Go to ```requirements/kafka_2.12-2.8.1/bin``` folder and run the following command:

```shell
./kafka-topics.sh --list --zookeeper 127.0.0.1:2181
```

This command should not throw any errors and should return an empty list (move to the next line without any visible output).

Once this command has run successfully, you can shut down the containers by going to ```requirements/docker``` and executing:

```shell
docker-compose down
```

