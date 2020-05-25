- docker run
```
docker run \
    -d \
    -p 80:80 \
    -p 443:443 \
    -p 22:22 \
    -v ~/data/docker/gitlab/config:/etc/gitlab \
    -v ~/data/docker/gitlab/log:/var/log/gitlab \
    -v ~/data/docker/gitlab/data:/var/opt/gitlab \
    --name gitlab \
    gitlab/gitlab-ce
```
- ⚠️注意：
- 预先将目标目录拷贝至本机
  - `docker cp gitlab:/etc/gitlab ~/data/docker/gitlab/config`
  - `docker cp gitlab:/var/log/gitlab ~/data/docker/gitlab/log`
  - `docker cp gitlab:/var/opt/gitlab ~/data/docker/gitlab/data`
