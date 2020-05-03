- docker run
```
docker run -d \
    -e POSTGRES_PASSWORD=chenlong \
    -e PGDATA=/var/lib/postgresql/data/pgdata \
    -v ~/data/docker/postgresql/data:/var/lib/postgresql/data \
    -p 5432:5432 \
    --name postgres \
    postgres
```
