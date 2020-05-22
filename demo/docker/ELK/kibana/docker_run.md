- docker run
```
docker run -d \
  -p 5601:5601 \
  -e "ELASTICSEARCH_URL=http://172.17.0.3:9200" \
  -e "ELASTICSEARCH_USERNAME=elastic" \
  -e "ELASTICSEARCH_PASSWORD=changeme" \
  -v ~/data/docker/kibana:/usr/share/kibana \
  --name kibana \
  kibana:7.4.2
```
- ⚠️注意：
- 预先将目标目录拷贝至本机：`docker cp kibana:/usr/share/kibana ~/data/docker/`
- 修改`config/kibana.yml`配置elasticsearc连接方式
