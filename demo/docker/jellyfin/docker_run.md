- docker run
````
docker run \
    -d \
    -p 8096:8096 \
    -v ~/data/docker/jellyfin/config:/config \
    -v ~/data/docker/jellyfin/media:/media \
    --name jellyfin \
    jellyfin/jellyfin
````
