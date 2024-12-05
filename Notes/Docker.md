# Docker Commands

## Basic Docker Commands:-

### Build
- Build an image from a Dockerfile: `docker build -t [image name] .`

### Run
- Run a container from an image: `docker run [image name]`


### List
- List running containers: `docker ps`
- List all containers (including stopped ones): `docker ps -a`


### Stop and Remove Containers
- Stop a running container: `docker stop [id]`
- Remove a stopped container: `docker rm [docker name]`


### Images
- List all images: `docker images`
- Delete an image: `docker rmi [image name]`


### Pull and Run Images
- Pull and run an image in one step: `docker run [image name]`
- Pull an image without running it: `docker pull [image name]`



