# Threat Intelligence Platform: TheHive, Cortex, and MISP Docker Deployment 🚨🔍

## 🌐 Project Overview

This project demonstrates a comprehensive threat intelligence and security analysis platform deployed on Ubuntu using Docker Compose. The solution integrates three powerful open-source tools:
- TheHive
- Cortex
- MISP (Malware Information Sharing Platform)

### 🛡️ Key Components    
- **TheHive**: Security incident management and response platform
- **Cortex**: Powerful observable analysis and active response engine
- **MISP**: Threat intelligence sharing and collaborative platform

## 🚀 Prerequisites

### System Requirements
- Ubuntu Server (20.04 LTS or later recommended)
- Docker Engine
- Docker Compose
- Minimum Recommended Specs:
  - 8 GB RAM
  - 4 CPU Cores
  - 100 GB SSD Storage

### 🔧 Required Installations
```bash
sudo apt update
sudo apt install docker.io docker-compose
sudo usermod -aG docker $USER
```

## 📦 Project Structure

```
threat-intel-project/
│
├── docker-compose.yml        # Main Docker Compose configuration
├── .env                      # Environment variables
├── data/                     # Persistent data volumes
│   ├── thehive/
│   ├── cortex/
│   └── misp/
└── config/                   # Configuration files
    ├── thehive.conf
    ├── cortex.conf
    └── misp.conf
```

## 🛠️ Docker Compose Configuration

### Key Configuration Highlights
- Centralized service orchestration
- Persistent data storage
- Integrated networking
- Security-focused deployment

### Sample Docker Compose Snippet
```yaml
version: '3.8'
services:
  thehive:
    image: thehiveproject/thehive:latest
    # Additional configuration...
  
  cortex:
    image: thehiveproject/cortex:latest
    # Additional configuration...
  
  misp:
    image: misp/misp-docker:latest
    # Additional configuration...
```

## 🔐 Security Considerations
- Use strong, unique passwords
- Implement network-level access controls
- Regularly update Docker images
- Configure HTTPS/TLS for all services
- Implement proper authentication mechanisms

## 🚦 Deployment Steps

1. Clone the repository
```bash
git clone https://github.com/your-username/threat-intel-project.git
cd threat-intel-project
```

2. Configure Environment Variables
```bash
cp .env.example .env
# Edit .env with your specific configurations
nano .env
```

3. Launch the Platform
```bash
docker-compose up -d
```

4. Access Services
- TheHive: `https://[YOUR_SERVER_IP]:9000`
- Cortex: `https://[YOUR_SERVER_IP]:9001`
- MISP: `https://[YOUR_SERVER_IP]:443`

## 🔍 Post-Deployment Setup
- Configure initial user accounts
- Set up API keys
- Configure analyzer plugins in Cortex
- Establish MISP sharing communities

## 📊 Monitoring & Maintenance

### Useful Docker Commands
```bash
# View running containers
docker-compose ps

# Check logs
docker-compose logs -f [service_name]

# Update images
docker-compose pull
docker-compose up -d
```

## 🆘 Troubleshooting
- Check Docker logs for specific service issues
- Verify network configurations
- Ensure all required ports are open
- Validate environment variable settings



## 🤝 Contributing
Contributions, issues, and feature requests are welcome!

##THANK YOU https://github.com/ls111-cybersec/ls111-cybersec FOR THE GUIDANCE
