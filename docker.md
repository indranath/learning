# Simple Docker Commands #

## Images ##

Download Image from public registry

	docker pull <owner>/<repository>:<tagname>
	docker pull ubuntu:14.04
	docker pull atlassian/stash:latest

List downloaded named images

	docker images

List downloaded ALL images

	docker images -a

## Containers ##

Create a container from an image with an interactive terminal and auto remove container at exit

	docker run -it --rm <image> <command> <arguments>
	docker run -it --rm ubuntu:14.04 /bin/bash

Create a container and run it in the background as a daemon

	docker run -d <image> <command> <arguments>
	docker run -d ubuntu:14.04 ping 8.8.8.8

List running containers

	docker ps

View the standard output log of a container

	docker logs <container-id/name>

Opening a interactive terminal in a running container

	docker exec -it <container-id/name> <command> <arguments>
	docker exec -it gloomy_shockley /bin/bash

Stop a running container

	docker stop <container-id/name>

## Versions ##

### Checking boot2docker version ###

	boot2docker version

Output:

	Boot2Docker-cli version: v1.5.0
	Git commit: ccd9032

### Checking docker version ###

	docker version

Output:

	Client version: 1.5.0
	Client API version: 1.17
	Go version (client): go1.4.1
	Git commit (client): a8a31ef
	OS/Arch (client): linux/amd64
	Server version: 1.5.0
	Server API version: 1.17
	Go version (server): go1.4.1
	Git commit (server): a8a31ef

