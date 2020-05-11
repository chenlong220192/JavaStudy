- docker run
```
docker run \
    -d \
    -p 2368:2368 \
    -v ~/data/docker/ghost/config.production.json:/var/lib/ghost/config.production.json \
    -v ~/data/docker/ghost/content:/var/lib/ghost/content \
    -e url=http://106.14.180.184/
    -e NODE_ENV=production \
    --name ghost \
    ghost
```
