- docker run
```
docker run \
    -d \
    -p 3306:3306 \
    -e MYSQL_ROOT_PASSWORD=chenlong \
    -v ~/data/docker/mysql_5.7.28/etc/mysql:/etc/mysql \
    -v ~/data/docker/mysql_5.7.28/var/lib/mysql:/var/lib/mysql \
    --name mysql_5.7.28 \
    mysql:5.7.28
```
- ⚠️注意：
- 预先将目标目录拷贝至本机
  - `docker cp mysql_5.7.28:/etc/mysql/ ~/data/docker/mysql_5.7.28/etc/`
  - `docker cp mysql_5.7.28:/var/lib/mysql ~/data/docker/mysql_5.7.28/var/lib/`
