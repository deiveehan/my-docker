# Build a simple apache web server on a docker image.

#### Create the docker file as below
[Dockerfile](Dockerfile)

```shell script
docker build . -t deiveehan/sampledockerimage
docker run -it -d -p 82:80 deiveehan/sampledockerimage
```
