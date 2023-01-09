# Install Docker Desktop and WSL2
https://docs.docker.com/desktop/install/windows-install/

# Run Kafka with Docker
> :warning: Twitter API keys are needed in an .env file

https://www.conduktor.io/kafka/how-to-start-kafka-using-docker

# Commands to run Kafka and Zookeper

```docker-compose -f zk-single-kafka-single.yml up -d```

## Check that both services are running
```docker-compose -f zk-single-kafka-single.yml ps```

## Running commands on Kafka instance on Docker

```docker exec -it kafka1 /bin/bash```

Then, from within the container, run Kafka commands without .sh
```kafka-topics --version```

## Create topic to store event

```kafka-topics --create --topic twitter --bootstrap-server localhost:9092```

## Display information on partition count etc

```kafka-topics --describe --topic twitter --bootstrap-server localhost:9092```

# Python code 

```python producer.py```
```python consumer.py```

# Stopping Kafka
```docker-compose -f zk-single-kafka-single.yml stop```


https://lorenagongang.com/sentiment-analysis-on-streaming-twitter-data-using-kafka-spark-structured-streaming-and-python-part-1
