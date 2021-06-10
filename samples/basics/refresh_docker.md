# Docker basics

# 1. Creating a ubuntu docker image and runnign apache2 on top of that image. 

```shell script
docker run -it -d ubuntu
docker images
docker ps
docker exec -it fa7e559e8307 bash
apt-get update
apt-get install apache2
service apache2 status
service apahce2 start
service apache2 status

# Saving the above configuration in a separate image container
docker commit fa7e559e8307 deiveehan/sampletestimage
docker run -it -d deiveehan/sampletestimage
docker ps 
docker exec -it <process-id>

service apache2 status
service apahce2 start
service apache2 status

# Login to docker hub
docker login
docker push deiveehan/sampletestimage:latest

# Removing the docker image
docker ps
docker rm -f <processid>

# Removing all containers
docker rm -f $(docker ps -a -q)
docker rmi deiveehan/sampletestimage
docker container prune
```

# 2. Running commands 
```shell script
docker  run ubuntu sleep 30

```

