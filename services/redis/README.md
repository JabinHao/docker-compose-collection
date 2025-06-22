# Redis 7.0.9

A high-performance, in-memory data structure store used as a database, cache, and message broker.

## Quick Start

1. Copy environment file:
```bash
cp .env.example .env
```

2. Edit `.env` with your configurations:
```bash
# Set your Redis password
REDIS_PASSWORD=your_secure_password
```

3. Start Redis:
```bash
docker-compose up -d
```

## Configuration

- **Image**: redis:7.0.9
- **Port**: 6379 (configurable via REDIS_PORT)
- **Password**: Set via REDIS_PASSWORD environment variable
- **Data Volume**: Persistent data storage

## Environment Variables

| Variable | Default | Description |
|----------|---------|-------------|
| REDIS_PASSWORD | defaultpassword | Redis authentication password |
| REDIS_PORT | 6379 | Redis server port |
| REDIS_DATA_PATH | ./data/redis | Path for data persistence |
| REDIS_NETWORK_IP | 172.30.2.1 | Container IP address |

## Usage

Connect to Redis:
```bash
docker exec -it redis7 redis-cli -a your_password
```

## Notes

- Ensure the data directory has proper permissions
- Change the default password for production use
- Data is persisted in the specified volume
