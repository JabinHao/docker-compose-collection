# Apache Kafka 4.0

A distributed streaming platform for building real-time data pipelines and streaming applications.

## Quick Start

1. Copy environment file:
```bash
cp .env.example .env
```

2. Start Kafka:
```bash
docker-compose up -d
```

## Configuration

- **Image**: bitnami/kafka:4.0
- **Port**: 9092
- **Mode**: KRaft (no Zookeeper required)
- **Data Volume**: Persistent data storage

## Environment Variables

| Variable | Default | Description |
|----------|---------|-------------|
| KAFKA_PORT | 9092 | Kafka broker port |
| KAFKA_DATA_PATH | ./data/kafka | Path for data persistence |
| KAFKA_NETWORK_IP | 172.30.3.1 | Container IP address |

## Usage

### Create a Topic
```bash
docker exec -it kafka kafka-topics.sh --create --topic test-topic --bootstrap-server localhost:9092
```

### List Topics
```bash
docker exec -it kafka kafka-topics.sh --list --bootstrap-server localhost:9092
```

### Producer
```bash
docker exec -it kafka kafka-console-producer.sh --topic test-topic --bootstrap-server localhost:9092
```

### Consumer
```bash
docker exec -it kafka kafka-console-consumer.sh --topic test-topic --bootstrap-server localhost:9092 --from-beginning
```

## Notes

- Uses KRaft mode (no Zookeeper dependency)
- Data is persisted in the specified volume
- Default configuration allows plaintext connections
- Suitable for development environments
