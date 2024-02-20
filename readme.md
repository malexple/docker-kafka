## Run docker compose

```bash
docker compose -f docker-compose.yml up -d
```

![image-20240220131640819](readme.assets/image-20240220131640819.png)

![image-20240220131753670](readme.assets/image-20240220131753670.png)

## Run console in docker container
```bash
docker exec -it kafka /bin/sh
```

## Using kafka

1. Run Intellij Idea and add configuration

   ![image-20240220132918033](readme.assets/image-20240220132918033.png)

2. Create topic

   ![image-20240220133022146](readme.assets/image-20240220133022146.png)

   ![image-20240220133246208](readme.assets/image-20240220133246208.png)

### Create Kafka topic

```
kafka-topics.sh --create --zookeeper zookeeper:2181 --replication-factor 1 --partitions 1 --topic quickstart
```

### Start Producer app (CLI)

```
kafka-console-producer.sh --topic quickstart --bootstrap-server localhost:9092
```

### Start consumer app (CLI)

```
kafka-console-consumer.sh --topic quickstart --from-beginning --bootstrap-server localhost:9092
```