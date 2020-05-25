- docker run
```
docker run -d \
  -p 9200:9200 -p 9300:9300 \
  -e "discovery.type=single-node" \
  -v ~/data/docker/ELK/elasticsearch:/usr/share/elasticsearch \
  --name elasticsearch \
  docker.elastic.co/elasticsearch/elasticsearch:7.7.0
```
- ⚠️注意：
- 预先将目标目录拷贝至本机：`docker cp elasticsearch:/usr/share/elasticsearch ~/data/docker/ELK/`
