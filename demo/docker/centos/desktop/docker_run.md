- docker run
````
docker run -d \
  -it \
  --name=centos_desktop \
  --privileged=true \
  -v /sys/fs/cgroup:/sys/fs/cgroup:ro \
  -p 80:80 \
  local/c7-desktop
````
