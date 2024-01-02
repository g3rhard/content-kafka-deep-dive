# content-kafka-deep-dive

- Start project

  ```sh
  export DOCKER_DEFAULT_PLATFORM=linux/amd64
  docker compose up -d --remove-orphans
  ```

## Kafka topics

- Create test topic from zookeep service

  ```sh
  docker exec -it content-kafka-deep-dive-zookeep1-1 bash
  kafka-topics --bootstrap-server localhost:9092 --create --topic test --partitions 3 --replication-factor 1
  ```

- List topics

  ```sh
  docker exec -it content-kafka-deep-dive-zookeep1-1 bash
  kafka-topics --bootstrap-server localhost:9092 --list
  ```

- Describe topic

  ```sh
  docker exec -it content-kafka-deep-dive-zookeep1-1 bash
  kafka-topics --bootstrap-server localhost:9092 --create --topic test --describe
  ```
