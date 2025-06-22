# Docker Compose Collection 🐳

A curated collection of Docker Compose files and scripts for quick deployment of common services and applications.

## 📋 Table of Contents

- [Overview](#overview)
- [Quick Start](#quick-start)
- [Services Available](#services-available)
- [Directory Structure](#directory-structure)
- [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)

## 🎯 Overview

This repository contains a collection of production-ready Docker Compose configurations for popular services and applications. Each service is organized in its own directory with comprehensive documentation and example configurations.

## 🚀 Quick Start

1. Clone this repository:
```bash
git clone https://github.com/JabinHao/docker-compose-collection.git
cd docker-compose-collection
```

2. Navigate to the service you want to deploy:
```bash
cd services/[service-name]
```

3. Copy and customize the environment file:
```bash
cp .env.example .env
# Edit .env with your specific configuration
```

4. Deploy the service:
```bash
docker-compose up -d
```

## 📦 Services Available

> 🚧 This section will be updated as services are added to the collection.

### Development Tools
- [ ] Database (PostgreSQL, MySQL, MongoDB)
- [ ] Redis
- [ ] Elasticsearch + Kibana
- [ ] Jenkins
- [ ] GitLab

### Web Services
- [ ] Nginx
- [ ] Traefik
- [ ] Caddy

### Monitoring & Logging
- [ ] Prometheus + Grafana
- [ ] ELK Stack
- [ ] Jaeger

### Self-hosted Applications
- [ ] Nextcloud
- [ ] WordPress
- [ ] Ghost
- [ ] Portainer

## 📁 Directory Structure

```
docker-compose-collection/
├── README.md
├── LICENSE
├── services/
│   ├── nginx/
│   │   ├── docker-compose.yml
│   │   ├── .env.example
│   │   ├── config/
│   │   └── README.md
│   ├── postgres/
│   │   ├── docker-compose.yml
│   │   ├── .env.example
│   │   ├── init/
│   │   └── README.md
│   └── ...
├── scripts/
│   ├── backup.sh
│   ├── cleanup.sh
│   └── health-check.sh
└── docs/
    ├── troubleshooting.md
    └── best-practices.md
```

## 📖 Usage

Each service directory contains:

- `docker-compose.yml` - Main compose file
- `.env.example` - Example environment variables
- `README.md` - Service-specific documentation
- `config/` - Configuration files (if needed)
- Additional scripts or files as required

### Environment Variables

Most services use environment variables for configuration. Always copy `.env.example` to `.env` and customize the values before deployment.

### Networking

Services are configured to use custom Docker networks to ensure proper isolation and communication.

### Data Persistence

Persistent data is stored in named volumes or bind mounts as appropriate for each service.

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request. Here are some ways you can contribute:

1. Add new service configurations
2. Improve existing configurations
3. Fix bugs or issues
4. Enhance documentation
5. Add useful scripts

### Contribution Guidelines

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/new-service`)
3. Follow the existing directory structure and naming conventions
4. Include comprehensive documentation
5. Test your configurations
6. Commit your changes (`git commit -am 'Add new service: ServiceName'`)
7. Push to the branch (`git push origin feature/new-service`)
8. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## ⭐ Support

If you find this collection useful, please consider giving it a star! It helps others discover the project.

## 🔗 Related Projects

- [Awesome Docker](https://github.com/veggiemonk/awesome-docker)
- [Docker Official Images](https://github.com/docker-library/official-images)

---

**Note**: Always review and understand the configurations before deploying to production environments. Update default passwords and security settings as needed.