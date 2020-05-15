- docker run
```
docker run \
    -d \
    -p 6379:6379 \
    -v ~/data/docker/redis:/data \
    --name redis \
    redis
```
