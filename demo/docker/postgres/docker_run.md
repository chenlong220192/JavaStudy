- docker run
```
docker run -d \
    -e POSTGRES_PASSWORD=chenlong \
    -e PGDATA=/var/lib/postgresql/data/pgdata \
    -v ~/data/docker/postgresql/:/var/lib/postgresql/ \
    -p 5432:5432 \
    --name postgres \
    postgres
```
- ⚠️注意：
- 预先将目标目录拷贝至本机
  - `docker cp postgres:/var/lib/postgresql/ ~/data/docker/postgresql`
