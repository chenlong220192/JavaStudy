- docker run
````
docker run \
    -d \
    -p 3306:3306 \
    -e MYSQL_ROOT_PASSWORD=chenlong \
    -v ~/data/docker/mysql5.7.28/etc/mysql:/etc/mysql \
    -v ~/data/docker/mysql5.7.28/var/lib/mysql:/var/lib/mysql \
    --name mysql_5.7.28 \
    mysql:5.7.28
````
