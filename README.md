# Cowrie honeypot

It's an integration of the popular Cowrie honeypot with Elastic Stack, which includes:
- Elastic Search
- Kibana
- Filebeat

You can read more about Cowrie in their official [repository](https://github.com/cowrie/cowrie)

## How to install
You need to have Docker Desktop or Docker Compose installed on your machine.

```bash
# clone project
git clone https://github.com/RykerWilder/cowrie-honeypot

cd cowrie-honeypot

# to create containers
docker compose up -d 

# to check container status
docker compose ps

# to stop containers
docker compose stop

# to destroy container
docker compose down
```

After the `docker compose up -d` command has pulled all the services and is successful when checked with the `docker compose ps` command, Kibana will be available on [localhost:](http://localhost:5601), Elasticsearch on http://localhost:9200, and you will be able to connect to the honeypot, from a new terminal, via the command `ssh root@localhost -p 2222`.