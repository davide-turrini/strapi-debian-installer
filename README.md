# strapi-debian-installer 🚀
Tested on AWS Free tier eligible `Debian10-1vCPU-1GB` with 8GB SSD and followinf firewall conf:

Incoming traffic:
- SSH TCP 22 OPEN ⚠️
- TCP 1337 OPEN ⚠️

Outgoing traffic:
- ALL OPEN ⚠️

## Steps:

### 1. Install docker (see [doc](https://docs.docker.com/engine/install/debian/)) ⬇️
```bash
curl https://raw.githubusercontent.com/davide-turrini/strapi-debian-installer/master/install.sh > install.sh && chmod +x install.sh && sudo ./install.sh && rm -rf install.sh
```

### 2. Download docker compose file (see [doc](https://strapi.io/documentation/developer-docs/latest/setup-deployment-guides/installation/docker.html#creating-a-strapi-project)) ⬇️
```bash
curl https://raw.githubusercontent.com/davide-turrini/strapi-debian-installer/master/docker-compose.yaml > docker-compose.yaml
```

### 3. Build image (see [doc](https://strapi.io/documentation/developer-docs/latest/setup-deployment-guides/installation/docker.html#creating-a-strapi-project)) 🛠️
```bash
docker-compose pull
```

### 4. Create container (see [doc](https://strapi.io/documentation/developer-docs/latest/setup-deployment-guides/installation/docker.html#creating-a-strapi-project)) ⏯️
Execute Docker image detaching the terminal
```bash
docker-compose up -d
```
Execute Docker image without detaching the terminal
```bash
docker-compose up
```

