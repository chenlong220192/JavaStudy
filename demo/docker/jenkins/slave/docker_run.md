- slave-01
````
docker run -d -it \
    --name=jenkins-slave-01 \
    -v ~/data/docker/jenkins-slave-01:/var/jenkins_home \
    -v ~/data/docker/jenkins-slave-01/root:/root \
    local/centos7-jenkins-slave
````
- slave-02
````
docker run -d -it \
    --name=jenkins-slave-02 \
    -v ~/data/docker/jenkins-slave-02:/var/jenkins_home \
    -v ~/data/docker/jenkins-slave-02/root:/root \
    local/centos7-jenkins-slave
````
