# MySQL 8.0.30

A powerful, open-source relational database management system.

## Quick Start

1. Copy environment file:
```bash
cp .env.example .env
```

2. Edit `.env` with your configurations:
```bash
# Set your MySQL root password
MYSQL_ROOT_PASSWORD=your_secure_password
```

3. Start MySQL:
```bash
docker-compose up -d
```

## Configuration

- **Image**: mysql:8.0.30
- **Port**: 3307 (external) -> 3306 (internal)
- **Authentication**: mysql_native_password
- **Data Volume**: Persistent data storage

## Environment Variables

| Variable | Default | Description |
|----------|---------|-------------|
| MYSQL_ROOT_PASSWORD | defaultpassword | MySQL root user password |
| MYSQL_PORT | 3307 | External port mapping |
| MYSQL_DATA_PATH | ./data/mysql | Path for data persistence |
| MYSQL_NETWORK_IP | 172.30.1.1 | Container IP address |

## Usage

Connect to MySQL:
```bash
# From host
mysql -h localhost -P 3307 -u root -p

# From container
docker exec -it mysql8 mysql -u root -p
```

## Notes

- Default port is mapped to 3307 to avoid conflicts
- Data is persisted in the specified volume
- Uses mysql_native_password for compatibility
- Change default password for production use
