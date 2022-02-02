# Docker Postgres Setup

## Getting Started

1. Clone this repo
2. Setup Volumes for Containers

```
docker volume create --name pgdb-data -d local
docker volume create --name pgadmin4-data -d local
```

3. Setup Network `pg-net`

```
docker network create --driver bridge postgres-net
```

4. Start containers

```
docker-compose up --build -d
```

* Shutdown with: `docker-compose down`