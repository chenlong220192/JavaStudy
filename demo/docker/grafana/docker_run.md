- docker run
```
docker run -d \
  -p 3000:3000 \
  -e GF_SERVER_ROOT_URL=http://grafana.server.name \
  -e GF_SECURITY_ADMIN_PASSWORD=1234 \
  -v ~/data/docker/grafana:/usr/share/grafana \
  --name grafana \
  grafana/grafana
```
- ⚠️注意：
- 预先将目标目录拷贝至本机：`docker cp grafana:/usr/share/grafana ~/data/docker/`
