- docker run
```
docker run -d \
  -p 5601:5601 \
  -v ~/data/docker/kibana:/usr/share/kibana \
  --name kibana \
  docker.elastic.co/kibana/kibana:7.7.0
```
- ⚠️注意：
- 预先将目标目录拷贝至本机：`docker cp kibana:/usr/share/kibana ~/data/docker/`
- 修改`config/kibana.yml`配置elasticsearc连接方式
  - elasticsearch.hosts: [ "http://ip:port" ]
  - elasticsearch.username: elastic
  - elasticsearch.password: changeme
