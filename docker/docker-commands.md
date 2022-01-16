---
description: Some most frequently used Docker CLI commands
coverY: -275.5061179087876
---

# Docker CLI Commands

## Docker Build

#### <mark style="color:purple;">`docker build -t repository-name:version .`</mark>

`docker build -t my-service:latest .`

#### <mark style="color:purple;">`docker build -t registry/repository-name:version .`</mark>

`docker build -t registry.azurecr.io/my-service:latest .`

#### <mark style="color:purple;">`docker build -t repository-name-1:version -t repository-name-2:version .`</mark>

`docker build -t my-service-1:1.0.0 -t my-service-2:1.0.0 .`

## Docker Tag

#### <mark style="color:purple;">`docker tag exiting-repository-name:version new-repository-name:version`</mark>

`docker tag my-service:latest registry.azurecr.io/my-service:latest`

## Docker Push

#### <mark style="color:purple;">`docker push registry/new-repository-name:version`</mark>

`docker push registry.azurecr.io/my-service:latest`

## Docker Image

#### List Images

<mark style="color:purple;">`docker images`</mark>

<mark style="color:purple;">`docker images -a`</mark>

<mark style="color:purple;">`docker image ls`</mark>

<mark style="color:purple;">`docker image ls -a`</mark>

#### Remove Image(s)

#### <mark style="color:purple;">`docker rmi <image-id(s) | image-name(s)>`</mark>

* `docker rmi hello-world`
* `docker rmi hello-world, order-service, 0706874044f0`

#### Remove all images

#### <mark style="color:purple;">`docker rmi $(docker images -aq)`</mark>

## Docker Container

#### List Containers

<mark style="color:purple;">`docker ps`</mark>

<mark style="color:purple;">`docker ps -a`</mark>

#### Stop Container(s)

#### <mark style="color:purple;">`docker stop <container-id(s) | container-name(s)>`</mark>

* `docker stop hello-world`
* `docker stop hello-world, order-service, item-service`

#### <mark style="color:purple;">`docker stop $(docker ps -aq)`</mark>

#### Remove Container(s)

#### <mark style="color:purple;">`docker rm <container-id(s) | container-name(s)>`</mark>

* `docker rm hello-world`
* `docker rm hello-world, order-service, item-service`

#### Remove all containers

<mark style="color:purple;">`docker rm $(docker ps -aq)`</mark>

#### Look what's happening inside container from <mark style="color:orange;">outside</mark>

<mark style="color:purple;">`docker container top CONTAINER`</mark>

<mark style="color:purple;">`docker container inspect CONTAINER`</mark>

<mark style="color:purple;">`docker container stats CONTAINER [CONTAINER...]`</mark>

#### Look what's happening inside container from <mark style="color:orange;">inside</mark>

<mark style="color:purple;">`docker container run -it --name nginx -p 80:80 nginx bash`</mark>

<mark style="color:purple;">`docker container run exec -it nginx bash`</mark>

## Docker Run

#### <mark style="color:purple;">`docker run -d --name my-service`</mark><mark style="color:orange;">**`-p host's-port:container's-port`**</mark><mark style="color:purple;">`my-service`</mark>

* `-d` or `--detach`: run container in detached/background mode and print container ID
* `-p` or `--publish` : bind outbound port to inbound port outbound:inbound i.e. 80:8080
* `--name` : assign a name to the container
* `docker run -d --name my-service`**`-p 80:8080`**` ``my-service`

## Docker Network

#### <mark style="color:purple;">`docker network create network-name`</mark>

creates **bridge** type of network with name: network-name

#### <mark style="color:purple;">`docker network create -d overlay network-name`</mark>

* creates **overlay** type of network with name: network-name
* if `-d` is not specified the default network type is **bridge**

#### <mark style="color:purple;">`docker network ls`</mark>

lists all the networks the Engine `daemon` knows about&#x20;

#### <mark style="color:purple;">`docker network ls --no-trunc`</mark>

lists all the networks with full network ID

#### <mark style="color:purple;">`docker network inspect network1 [network2 network3 ...]`</mark>

returns information about one or more networks

## Docker Volume

#### <mark style="color:purple;">`docker volume create hello`</mark>

creates hello named **local** type of volume

#### <mark style="color:purple;">`docker volume ls`</mark>

lists all volumes

## Docker Logs

#### <mark style="color:purple;">`docker logs CONTAINER`</mark>

retrieves logs present at the time of execution

#### <mark style="color:purple;">`docker logs -f CONTAINER`</mark>

follows logs output

#### <mark style="color:purple;">`docker logs --tail|-n CONTAINER`</mark>

number of lines to show from the end of the logs

## Docker Inspect

#### <mark style="color:purple;">`docker inspect NAME|ID [NAME|ID...]`</mark>

returns low-level information of docker objects

## Docker exec

#### <mark style="color:purple;">`docker exec [OPTIONS] CONTAINER COMMAND [ARGS...]`</mark>

* `docker exec -it my-container /bin/sh` or
* `docker exec -i -t my-container /bin/sh`
* run a command in running container
* `-i` : keep STDIN open even if not attached
* `-t` : allocate a pseudo-TTY
