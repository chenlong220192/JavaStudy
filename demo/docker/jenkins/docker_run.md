- docker run
````
docker run \
    -d \
    -p 8080:8080 \
    -p 50000:50000 \
    -v ~/data/docker/jenkins:/var/jenkins_home \
    --name jenkins \
    jenkins/jenkins
````
