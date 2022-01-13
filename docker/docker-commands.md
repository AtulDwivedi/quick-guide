# docker-commands

## Docker

| Command                                | Description                                           |
| -------------------------------------- | ----------------------------------------------------- |
| `docker build -t friendlyhello .`      | Create image using this directory's Dockerfile        |
| `docker run -p 4000:80 friendlyhello`  | Run "friendlyhello" mapping port 4000 to 80           |
| docker run -d -p 4000:80 friendlyhello | Same thing, but in detached mode                      |
| docker login                           | Log in this CLI session using your Docker credentials |
| docker tag  username/repository:tag    | Tag  for upload to registry                           |
| docker push username/repository:tag    | Upload tagged image to registry                       |
| docker run username/repository:tag     | Run image from a registry                             |

## Docker Container

| Command                                          | Description                                  |
| ------------------------------------------------ | -------------------------------------------- |
| docker container ls                              | List all running containers                  |
| docker container ls -a                           | List all containers, even those not running  |
| docker container stop                            | Gracefully stop the specified container      |
| docker container kill                            | Force shutdown of the specified container    |
| docker container rm                              | Remove specified container from this machine |
| docker container rm $(docker container ls -a -q) | Remove all containers                        |
| `docker container rm $(docker container ls -aq)` |                                              |

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
