# Docker Commands

## Docker Build



<mark style="color:purple;">`docker build -t repository-name:version .`</mark>

<mark style="color:purple;">`docker build -t repository-name:version -t username/repository-name:version .`</mark>

Example:

* `docker build -t myservice:latest .`
* `docker build -t routinecart.azurecr.io/myservice:latest .`
* `docker build -t myservice:latest -t routinecart.azurecr.io/myservice:latest .`

| Command                                  | Description                                           |
| ---------------------------------------- | ----------------------------------------------------- |
| `docker build -t friendlyhello .`        | Create image using this directory's Dockerfile        |
| `docker run -p 4000:80 friendlyhello`    | Run "friendlyhello" mapping port 4000 to 80           |
| `docker run -d -p 4000:80 friendlyhello` | Same thing, but in detached mode                      |
| `docker login`                           | Log in this CLI session using your Docker credentials |
| `docker tag  username/repository:tag`    | Tag  for upload to registry                           |
| `docker push username/repository:tag`    | Upload tagged image to registry                       |
| d`ocker run username/repository:tag`     | Run image from a registry                             |

## Docker Container

#### List Containers

<mark style="color:purple;">`docker ps`</mark>

<mark style="color:purple;">`docker ps -a`</mark>

#### Stop Container(s)

<mark style="color:purple;">`docker stop <container-id(s) | container-name(s)>`</mark>

Example:

* `docker stop hello-world`
* `docker stop hello-world, order-service, item-service`

#### Remove Container(s)

<mark style="color:purple;">`docker rm <container-id(s) | container-name(s)>`</mark>

Example:

* `docker rm hello-world`
* `docker rm hello-world, order-service, item-service`

## Docker Image

| Command                                                                                   | Description                              |
| ----------------------------------------------------------------------------------------- | ---------------------------------------- |
| docker image ls -a                                                                        | List all images on this machine          |
| docker image rm                                                                           | Remove specified image from this machine |
| docker image rm $(docker image ls -a -q)                                                  | Remove all images from this machine      |
| `docker image rm $(docker image ls -aq)`                                                  |                                          |
| `docker tag api-gateway-service:latest routinecart.azurecr.io/api-gateway-service:latest` | Tag docker image                         |
| `docker push routinecart.azurecr.io/api-gateway-service:latest`                           | Push docker image                        |

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
