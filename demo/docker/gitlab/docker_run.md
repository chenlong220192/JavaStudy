- docker run
```
docker run \
    -d \
    -p 80:80 \
    -p 443:443 \
    -p 22:22 \
    -v ~/data/docker/gitlab/config:/etc/gitlab \
    -v ~/data/docker/gitlab/logs:/var/log/gitlab \
    -v ~/data/docker/gitlab/data:/var/opt/gitlab \
    --name gitlab \
    gitlab/gitlab-ce
```
