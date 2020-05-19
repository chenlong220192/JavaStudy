- docker run
```
docker run \
  -v /:/rootfs:ro \
  -v /var/run:/var/run:rw \
  -v /sys:/sys:ro \
  -v /var/lib/docker/:/var/lib/docker:ro \
  -p 9092:8080 \
  --detach=true \
  --privileged=true \
  --name=cadvisor \
  google/cadvisor:latest
```
