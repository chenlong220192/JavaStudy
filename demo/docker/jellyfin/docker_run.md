- docker run
````
docker run \
    -d \
    -p 8096:8096 \
    -v ~/data/docker/jellyfin/config:/config \
    -v ~/data/docker/jellyfin/media:/media \
    -v ~/data/docker/jellyfin/cache:/cache \
    --name jellyfin \
    jellyfin/jellyfin
````
