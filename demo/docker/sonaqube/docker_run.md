- sonarqube最新版本
````
docker run \
      -d \
      -it \
      -p 9002:9000 \
      -v ~/data/docker/sonarqube/conf:/opt/sonarqube/conf \
      -v ~/data/docker/sonarqube/logs:/opt/sonarqube/logs \
      -v ~/data/docker/sonarqube/data:/opt/sonarqube/data \
      -v ~/data/docker/sonarqube/web:/opt/sonarqube/web \
      -v ~/data/docker/sonarqube/lib:/opt/sonarqube/lib \
      -v ~/data/docker/sonarqube/extensions:/opt/sonarqube/extensions \
      -v ~/data/docker/sonarqube/elasticsearch:/opt/sonarqube/elasticsearch \
      -e SONARQUBE_JDBC_USERNAME=postgres \
      -e SONARQUBE_JDBC_PASSWORD=chenlong \
      -e SONARQUBE_JDBC_URL="jdbc:postgresql://172.17.0.5:5432/sonarqube" \
      --name sonarqube \
      sonarqube
````

- sonarqube7.8社区版
````
docker run \
      -d \
      -it \
      -p 9003:9000 \
      -v ~/data/docker/sonarqube-7_8-community/conf:/opt/sonarqube/conf \
      -v ~/data/docker/sonarqube-7_8-community/logs:/opt/sonarqube/logs \
      -v ~/data/docker/sonarqube-7_8-community/data:/opt/sonarqube/data \
      -v ~/data/docker/sonarqube-7_8-community/web:/opt/sonarqube/web \
      -v ~/data/docker/sonarqube-7_8-community/lib:/opt/sonarqube/lib \
      -v ~/data/docker/sonarqube-7_8-community/extensions:/opt/sonarqube/extensions \
      -v ~/data/docker/sonarqube-7_8-community/elasticsearch:/opt/sonarqube/elasticsearch \
      -e SONARQUBE_JDBC_USERNAME=root \
      -e SONARQUBE_JDBC_PASSWORD=chenlong \
      -e SONARQUBE_JDBC_URL="jdbc:mysql://172.17.0.3:3306/sonarqube?useUnicode=true&characterEncoding=utf8&rewriteBatchedStatements=true&useConfigs=maxPerformance&useSSL=false" \
      --name sonarqube-7_8-community \
      sonarqube:7.8-community
````

***

- 默认账号密码：admin/admin
- ⚠️注意：需要提前将以上目录拷贝到响应卷
  - 例：`docker cp sonarqube:/opt/data ~/data/docker/sonarqube`
