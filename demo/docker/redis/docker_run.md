- docker run
```
docker run \
    -d \
    -p 6379:6379 \
    -v /Users/chenlong/data/docker/redis:/data \
    --name redis \
    redis
```
