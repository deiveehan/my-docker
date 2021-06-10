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
docker run deiveehan/docker-command sleep 15
# Notice that the sleep 10 is overwritten by the above command

# Only passing arguments and not all the commands again
docker build -f 2-Dockerfile . -t deiveehan/docker-command
docker run deiveehan/docker-command 5
# Note that the above command does not require to pass the sleep command as
# its already defined in the docker file. 

docker run deiveehan/docker-command
# You must be passing the entrypoint argument, the above command throws error

# Specifying a default value to avoid the above error
# Watch 3-Dockerfile. 
docker build -f 3-Dockerfile . -t deiveehan/docker-command
docker run deiveehan/docker-command
docker run deiveehan/docker-command 10

# You can override the entrypoint too
docker run --entrypoint echo deiveehan/docker-command 10
# in this case the sleep command is replaced by echo

```
