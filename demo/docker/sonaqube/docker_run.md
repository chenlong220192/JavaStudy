docker run \
  -d \
  -it \
  -p 9002:9000 \
  -v ~/data/docker/sonarqube/conf:/opt/sonarqube/conf \
  -v ~/data/docker/sonarqube/logs:/opt/sonarqube/logs \
  -v ~/data/docker/sonarqube/data:/opt/sonarqube/data \
  -v ~/data/docker/sonarqube/extensions:/opt/sonarqube/extensions \
  --name sonarqube \
  sonarqube

- 默认账号密码：admin/admin
- postgre
  - sonar.jdbc.url=jdbc:postgresql://172.17.0.3:5432/sonarqube
  - sonar.jdbc.username=postgres
  - sonar.jdbc.password=chenlong
