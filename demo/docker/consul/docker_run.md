- docker run
```
docker run -d -it \
    --name consul \
    -v ~/data/docker/consul/dc1:/consul/data \
    -e CONSUL_BIND_INTERFACE=eth0 \
    consul
```
- 加入新节点
```
docker run -d --name consul_agent01 -e CONSUL_BIND_INTERFACE=eth0 -v ~/data/docker/consul/agent01:/consul/data consul agent -dev -join=172.17.0.3
```
```
docker run -d --name consul_agent02 -e CONSUL_BIND_INTERFACE=eth0 -v ~/data/docker/consul/agent02:/consul/data consul agent -dev -join=172.17.0.3
```
