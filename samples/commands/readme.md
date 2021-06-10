## Commands and arguments


```shell script
docker run ubuntu
watch docker ps # in a separate window
docker run ubuntu sleep 10
# notice that the docker ps will stay alive for 10 seconds. 


# How to pass commands from a docker file. 
watch docker ps # in a separate window
docker build -f 1-Dockerfile . -t deiveehan/docker-command
docker images
docker run deiveehan/docker-command

# Override command that is present in the docker file

```
