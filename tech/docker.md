This concise cheat sheet serves as a practical reference for the most common Docker commands, designed to facilitate both newcomers and seasoned users in efficiently managing Docker containers, images, networks, and volumes. With sections covering everything from getting started with Docker, handling Docker containers and images, to advanced topics like Docker Compose and Docker security practices, it aims to streamline your Docker workflow and enhance security. For further details and advanced usage, refer to the [official Docker documentation](https://docs.docker.com/get-started/).

## Getting Started
### Getting started 
Create and run a container in background

```shell script 
$ docker run -d -p 80:80 docker/getting-started
```

----

- `-d` - Run the container in detached mode
- `-p 80:80` -  Map port 80 to port 80 in the container
- `docker/getting-started` - The image to use
{.marker-none}


Create and run a container in foreground
```shell script
$ docker run -it -p 8001:8080 --name my-nginx nginx
```

----

- `-it` - Interactive bash mode
- `-p 8001:8080` - Map port 8001 to port 8080 in the container
- `--name my-nginx` - Specify a name
- `nginx` - The image to use
{.marker-none}



### General commands 
| Example                             | Description                                      |
|-------------------------------------|--------------------------------------------------|
| `docker ps`                         | List running containers                          |
| `docker ps -a`                      | List all containers                              |
| `docker ps -s`                      | List running containers (with CPU / memory) |
| `docker images`                     | List all images                                  |
| `docker exec -it <container>  bash` | Connecting to container                          |
| `docker logs <container>`           | Shows container's console log                    |
| `docker stop <container>`           | Stop a container                                 |
| `docker restart <container>`        | Restart a container                              |
| `docker rm <container>`             | Remove a container                               |
| `docker port <container>`           | Shows container's port mapping                   |
| `docker top <container>`            | List processes                                   |
| `docker kill <container>`           | Kill a container                                 |

Parameter `<container>` can be container id or name




## Docker Containers
### Starting & Stopping
| Description                   | Example                             |
|-------------------------------|-------------------------------------|
| `docker start my-nginx`   | Starting                            |
| `docker stop my-nginx`    | Stopping                            |
| `docker restart my-nginx` | Restarting                          |
| `docker pause my-nginx`   | Pausing                             |
| `docker unpause my-nginx` | Unpausing                           |
| `docker wait my-nginx`    | Blocking a Container                |
| `docker kill my-nginx`    | Sending a SIGKILL                   |
| `docker attach my-nginx`  | Connecting to an Existing Container |



### Information

| Example                       | Description                            |
|-------------------------------|----------------------------------------|
| `docker ps`                   | List running containers                |
| `docker ps -a`                | List all containers                    |
| `docker logs my-nginx`    | Container Logs                         |
| `docker inspect my-nginx` | Inspecting Containers                  |
| `docker events my-nginx`  | Containers Events                      |
| `docker port my-nginx`    | Public Ports                           |
| `docker top my-nginx`     | Running Processes                      |
| `docker stats my-nginx`   | Container Resource Usage               |
| `docker diff my-nginx`    | Lists the changes made to a container. |


### Creating

```yaml
docker create [options] IMAGE
  -a, --attach               # attach stdout/err
  -i, --interactive          # attach stdin (interactive)
  -t, --tty                  # pseudo-tty
      --name NAME            # name your image
  -p, --publish 5000:5000    # port map (host:container)
      --expose 5432          # expose a port to containers
  -P, --publish-all          # publish all ports
      --link container:alias # linking
  -v, --volume `pwd`:/app    # mount (absolute paths needed)
  -e, --env NAME=hello       # env vars
```
#### Example
```shell script
$ docker create --name my_redis --expose 6379 redis:3.0.2
```


### Manipulating
Renaming a Container
```shell script
docker rename my-nginx my-nginx
```
Removing a Container
```shell script
docker rm my-nginx
```
Updating a Container
```shell script
docker update --cpu-shares 512 -m 300M my-nginx
```




## Docker Images
### Manipulating
| `Example`                          | Description                     |
|------------------------------------|---------------------------------|
| `docker images`                    | Listing images                  |
| `docker rmi nginx`                 | Removing an image               |
| `docker load < ubuntu.tar.gz`      | Loading a tarred repository     |
| `docker load --input ubuntu.tar`   | Loading a tarred repository     |
| `docker save busybox > ubuntu.tar` | Save an image to a tar archive  |
| `docker history`                   | Showing the history of an image |
| `docker commit nginx`              | Save a container as an image.   |
| `docker tag nginx eon01/nginx`     | Tagging an image                |
| `docker push eon01/nginx`          | Pushing an image                |


### Building Images
```shell script
$ docker build .
$ docker build github.com/creack/docker-firefox
$ docker build - < Dockerfile
$ docker build - < context.tar.gz
$ docker build -t eon/my-nginx .
$ docker build -f myOtherDockerfile .
$ curl example.com/remote/Dockerfile | docker build -f - .
```

## Dockerfile Instructions
### Common Instructions
| Instruction | Description                                                  |
|-------------|--------------------------------------------------------------|
| `FROM`      | Sets the Base Image for subsequent instructions              |
| `RUN`       | Execute commands in a new layer on top of the current image  |
| `CMD`       | Provide defaults for an executing container                  |
| `LABEL`     | Add metadata to an image (e.g., version, description)        |
| `EXPOSE`    | Inform Docker that the container listens on specified ports  |
| `ENV`       | Set environment variables                                    |
| `ADD`       | Copy files from a source to the container's filesystem       |
| `COPY`      | Copy new files or directories into the container             |
| `ENTRYPOINT`| Configure a container that will run as an executable         |
| `VOLUME`    | Create a mount point with the specified name                 |
| `USER`      | Set the UID (or username) to use when running the image      |
| `WORKDIR`   | Set the working directory for any `RUN`, `CMD`, `ENTRYPOINT`, `COPY`, and `ADD` instructions that follow it in the Dockerfile |
| `ARG`       | Define variables that users can pass at build-time to the builder |
| `ONBUILD`   | Add a trigger instruction when the image is used as the base for another build |

### Best Practices
- Use `.dockerignore` to exclude files not relevant to the build.
- Minimize the number of layers by combining instructions.
- Use multi-stage builds to reduce size and secure final images.
- Prefer `COPY` over `ADD` unless you need to add tar files or from URLs.

### Example Dockerfile
```Dockerfile
# Use an official Python runtime as a parent image
FROM python:3.7-slim

# Set the working directory in the container
WORKDIR /app

# Copy the current directory contents into the container at /app
COPY . /app

# Install any needed packages specified in requirements.txt
RUN pip install --trusted-host pypi.python.org -r requirements.txt

# Make port 80 available to the world outside this container
EXPOSE 80

# Define environment variable
ENV NAME World

# Run app.py when the container launches
CMD ["python", "app.py"]
```

## Volume Management
### Basic Volume Commands
| Command                                    | Description                                               |
|--------------------------------------------|-----------------------------------------------------------|
| `docker volume ls`                         | List all volumes                                          |
| `docker volume create <volume_name>`       | Create a new volume                                       |
| `docker volume inspect <volume_name>`      | Display detailed information on one or more volumes       |
| `docker volume rm <volume_name>`           | Remove one or more volumes                                |
| `docker volume prune`                      | Remove all unused volumes                                 |

### Advanced Volume Options
- **Create a Volume with Specific Options:**
  ```shell
  docker volume create --name <volume_name> --driver local \
    --opt type=tmpfs \
    --opt device=tmpfs \
    --opt o=size=100m,uid=1000


## Docker Networking
### Manipulating

Removing a network
```shell script
docker network rm MyOverlayNetwork
```
Listing networks
```shell script
docker network ls
```
Getting information about a network
```shell script
docker network inspect MyOverlayNetwork
```
Connecting a running container to a network
```shell script
docker network connect MyOverlayNetwork nginx
```
Connecting a container to a network when it starts
```shell script
docker run -it -d --network=MyOverlayNetwork nginx
```
Disconnecting a container from a network
```shell script
docker network disconnect MyOverlayNetwork nginx
```



### Creating Networks
```shell script
docker network create -d overlay MyOverlayNetwork

docker network create -d bridge MyBridgeNetwork

docker network create -d overlay \
  --subnet=192.168.0.0/16 \
  --subnet=192.170.0.0/16 \
  --gateway=192.168.0.100 \
  --gateway=192.170.0.100 \
  --ip-range=192.168.1.0/24 \
  --aux-address="my-router=192.168.1.5" \
  --aux-address="my-switch=192.168.1.6" \
  --aux-address="my-printer=192.170.1.5" \
  --aux-address="my-nas=192.170.1.6" \
  MyOverlayNetwork
```



## Clean Up
### Clean All
Cleans up dangling images, containers, volumes, and networks (ie, not associated with a container)
```shell
docker system prune
```

-------

Additionally, remove any stopped containers and all unused images (not just dangling images)

```shell
docker system prune -a
```



### Containers

Stop all running containers
```shell
docker stop $(docker ps -a -q)
```

Delete stopped containers
```shell
docker container prune
```

### Images

Remove all dangling (not tagged and is not associated with a container) images:
```shell
docker image prune
```

Remove all images which are not used by existing containers
```shell
docker image prune -a
```


### Volumes

```shell
docker volume prune
```
Remove all volumes not used by at least one container


## Docker Compose
### Basic Commands
Docker Compose simplifies the management of multi-container Docker applications. Here are some essential commands:


| Command                               | Description                                      |
|---------------------------------------|--------------------------------------------------|
| `docker-compose up`                   | Create and start containers                      |
| `docker-compose down`                 | Stop and remove containers, networks, images, and volumes |
| `docker-compose build`                | Build or rebuild services                        |
| `docker-compose logs`                 | View output from containers                      |
| `docker-compose restart`              | Restart all services                             |
| `docker-compose pull`                 | Pull service images                              |
| `docker-compose stop`                 | Stop services                                    |
| `docker-compose start`                | Start services                                   |
| `docker-compose run <service> <cmd>`  | Run a one-time command on a service              |
| `docker-compose exec <service> <cmd>` | Execute a command in a running container         |

### Other Useful
#### Configuration Files
- Primary: `docker-compose.yml`
- Overrides: `docker-compose.override.yml`

#### Versioning
- Specify the Compose file version at the top of the file: `version: '3'`

#### Services
Define services that make up your application so they can be run together in an isolated environment.

#### Volumes
Declare volumes for persistence or as shared directories between services.

#### Networks
Define networks to enable communication between containers.


## Docker Security Practices
### Security Scanning
- **Scan Images for Vulnerabilities:**
  ```shell
  docker scan <image_name>
  ```
  Use Docker's built-in scanning capabilities to identify security issues within your images.

### Running Containers Securely
- **Run as Non-Root User:**
  ```Dockerfile
  USER nonrootuser
  ```
  In your Dockerfile, specify a non-root user for running the container to limit privileges.

- **Use Read-Only Filesystems:**
  ```shell
  docker run --read-only <image_name>
  ```
  Where possible, run containers with a read-only filesystem to prevent modifications.

- **Limit Memory and CPU:**
  ```shell
  docker run --memory=500m --cpus=2 <image_name>
  ```
  Prevent resource abuse by limiting the memory and CPU usage of your containers.

### Secure Docker Daemon
- **Enable TLS:**
  Secure the Docker daemon by enabling TLS, ensuring that all communications are encrypted and authenticated.
  ```shell
  dockerd --tlsverify --tlscacert=ca.pem --tlscert=server-cert.pem --tlskey=server-key.pem -H=0.0.0.0:2376
  ```

### Networking Security
- **Use Custom Bridge Networks:**
  Create custom bridge networks to control which containers can communicate with each other.

### Best Practices
- Regularly update Docker and container applications to the latest versions.
- Apply the principle of least privilege in container permissions and capabilities.
- Use Docker Bench for Security to check for common best practices around deploying Docker containers in production.


## Miscellaneous
### Docker Hub
| Docker Syntax               | Description                         |
|-----------------------------|-------------------------------------|
| `docker search search_word` | Search docker hub for images.       |
| `docker pull user/image   ` | Downloads an image from docker hub. |
| `docker login             ` | Authenticate to docker hub          |
| `docker push user/image   ` | Uploads an image to docker hub.     |





### Registry commands

Login to a Registry

```shell script
$ docker login
$ docker login localhost:8080
```

Logout from a Registry

```shell script
$ docker logout
$ docker logout localhost:8080
```

Searching an Image

```shell script
$ docker search nginx
$ docker search nginx --stars=3 --no-trunc busybox
```

Pulling an Image

```shell script
$ docker pull nginx
$ docker pull eon01/nginx localhost:5000/myadmin/nginx
```

Pushing an Image

```shell script
$ docker push eon01/nginx
$ docker push eon01/nginx localhost:5000/myadmin/nginx
```



### Batch clean
|  Example                                     | Description                                            |
|-------------|---------------------------------------------|
`docker stop -f $(docker ps -a -q)` | Stopping all containers 
`docker rm -f $(docker ps -a -q)` |  Removing all containers
`docker rmi -f $(docker images -q)` | Removing all images





### Volumes

Check volumes
```shell script
$ docker volume ls
```
Cleanup unused volumes
```shell script
$ docker volume prune
```
