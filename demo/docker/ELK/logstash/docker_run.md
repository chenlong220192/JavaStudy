- docker run
```
docker run -d \
  -v ~/data/docker/logstash:/usr/share/logstash \
  --name logstash \
  logstash:7.4.2
```
- ⚠️注意：
- 预先将目标目录拷贝至本机：`docker cp logstash:/usr/share/logstash ~/data/docker/`
- 
