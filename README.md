# chroma-db-installation-docker
Docker based installation of Chroma DB in Digital Ocean Droplet

# Docker Compose Installation

Download Docker Compose:
```
sudo curl -L "https://github.com/docker/compose/releases/download/[latest-version]/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
```

Example for version 2.24.0-birthday.10:
```
sudo curl -L "https://github.com/docker/compose/releases/download/v2.24.0-birthday.10/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
```

Make the binary executable:
```
sudo chmod +x /usr/local/bin/docker-compose
```

Verify the installation:
```
docker-compose --version
```

Optionally, create a symlink if necessary:
```
sudo ln -s /usr/local/bin/docker-compose /usr/bin/docker-compose
```

# Chroma Installation

Refer to the Langchain Chroma documentation for detailed steps:
[Langchain Chroma Documentation](https://js.langchain.com/docs/integrations/vectorstores/chroma)

Clone the Chroma repository:
```
git clone https://github.com/chroma-core/chroma
cd chroma
docker-compose up -d --build
```

Test with Docker to ensure the server is running:
```
docker ps
```

You should see `chroma-server-1` running.

