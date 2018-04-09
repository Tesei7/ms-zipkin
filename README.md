# How to run re-create docker image

**mvn clean package docker:build**

# To run image

## Create network

**docker network create ms-net**

## Run image

**docker run
  -p 9411:9411
  --env PROFILE=dev
  --env SERVER_PORT=9411
  --env ZIPKIN_URI=http://ms-zipkin:9411
  --name ms-zipkin
  --network ms-net
  tesei7/ms-zipkin:latest**