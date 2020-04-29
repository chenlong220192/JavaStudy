- docker run
````
docker run \
    -d \
    -p 8081:8081 \
    -v /data/docker/nexus3:/nexus-data \
    --name nexus \
    sonatype/nexus3
````
