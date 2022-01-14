# Docker Commands

## Docker Build

<mark style="color:purple;">`docker build -t repository-name:version .`</mark>

<mark style="color:purple;">`docker build -t registry/repository-name:version .`</mark>

<mark style="color:purple;">`docker build -t repository-name-1:version -t repository-name-2:version .`</mark>

Example:

* `docker build -t my-service:latest .`
* `docker build -t registry.azurecr.io/my-service:latest .`
* `docker build -t my-service-1:1.0.0 -t my-service-2:1.0.0 .`

## Docker Tag

<mark style="color:purple;">`docker tag exiting-repository-name:version new-repository-name:version`</mark>

Example:

* `docker tag my-service:latest registry.azurecr.io/my-service:latest`

## Docker Push

<mark style="color:purple;">`docker push registry/new-repository-name:version`</mark>

Example:

* `docker push registry.azurecr.io/my-service:latest`

## Docker Container

#### List Containers

<mark style="color:purple;">`docker ps`</mark>

<mark style="color:purple;">`docker ps -a`</mark>

#### Stop Container(s)

<mark style="color:purple;">`docker stop <container-id(s) | container-name(s)>`</mark>

<mark style="color:purple;">`docker stop $(docker ps -aq)`</mark>

Example:

* `docker stop hello-world`
* `docker stop hello-world, order-service, item-service`

#### Remove Container(s)

<mark style="color:purple;">`docker rm <container-id(s) | container-name(s)>`</mark>

Example:

* `docker rm hello-world`
* `docker rm hello-world, order-service, item-service`

## Docker Image

#### List Images

<mark style="color:purple;">`docker images`</mark>

<mark style="color:purple;">`docker images -a`</mark>

<mark style="color:purple;">`docker image ls`</mark>

<mark style="color:purple;">`docker image ls -a`</mark>

#### Remove Images(s)

<mark style="color:purple;">`docker rmi <image-id(s) | image-name(s)>`</mark>

<mark style="color:purple;">`docker rmi $(docker images -aq)`</mark>

Example:

* `docker rmi hello-world`
* `docker rmi hello-world, order-service, 0706874044f0`

## Docker Run

## Docker Network

| Command                               | Description                                          |
| ------------------------------------- | ---------------------------------------------------- |
| `docker network create network-name`  | Create a network                                     |
| `docker network inspect network-name` | Display detailed information on one or more networks |

## Docker Volume

| Command                     | Description |
| --------------------------- | ----------- |
| `docker volume create name` | TBD         |

## Docker Logs

| Command                                   | Description |
| ----------------------------------------- | ----------- |
| `docker logs container-name/container-id` | TBD         |
