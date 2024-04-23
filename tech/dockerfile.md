This **Dockerfile Cheat Sheet** serves as a practical reference, detailing essential Dockerfile commands and [best practices](#best-practices) for creating, running, and managing Docker containers effectively. It covers everything from [basic commands](##basic-commands), [file handling](#working-with-files), and environment configuration to advanced features like multi-stage builds and health checks. Designed to be a go-to resource, it provides developers of all skill levels with the tools needed to build, deploy, and troubleshoot Docker containers, supplemented by links to further learning resources and community forums for ongoing support.

## Basic Commands
### FROM
- **Purpose**: Sets the base image for subsequent instructions. Every Dockerfile must start with a `FROM` command, except in the case of multi-stage builds.
- **Usage**: 
  ```dockerfile
  FROM <image>:<tag>
  ```
- **Example**:
  ```dockerfile
  FROM ubuntu:20.04
  ```

### RUN
- **Purpose**: Executes commands in a new layer on top of the current image and commits the results.
- **Usage**: 
  ```dockerfile
  RUN <command>
  ```
- **Example**:
  ```dockerfile
  RUN apt-get update && apt-get install -y python3
  ```

### CMD
- **Purpose**: Provides defaults for executing a container. There can only be one `CMD` instruction in a Dockerfile.
- **Usage**: 
  ```dockerfile
  CMD ["executable","param1","param2"]
  ```
- **Example**:
  ```dockerfile
  CMD ["echo", "Hello World"]
  ```

### LABEL
- **Purpose**: Adds metadata to an image such as version, description, or maintainer.
- **Usage**: 
  ```dockerfile
  LABEL <key>=<value> <key>=<value> ...
  ```
- **Example**:
  ```dockerfile
  LABEL version="1.0" description="This is an example."
  ```

### EXPOSE
- **Purpose**: Informs Docker that the container listens on the specified network ports at runtime. It is purely informational and does not actually publish the port.
- **Usage**: 
  ```dockerfile
  EXPOSE <port>
  ```
- **Example**:
  ```dockerfile
  EXPOSE 80
  ```

### ENV
- **Purpose**: Sets environment variables.
- **Usage**: 
  ```dockerfile
  ENV <key>=<value>
  ```
- **Example**:
  ```dockerfile
  ENV MY_NAME="John Doe"
  ```


## Working with Files
### COPY
- **Purpose**: Copies new files or directories from the source location on the host into the filesystem of the container at the specified path.
- **Usage**:
  ```dockerfile
  COPY [--chown=<user>:<group>] <src>... <dest>
  ```
- **Example**:
  ```dockerfile
  COPY . /app
  ```
- **Notes**: The `COPY` command only takes local files in the build context or files in stages in multi-stage builds.

### ADD
- **Purpose**: Similar to `COPY`, but with the ability to handle remote URLs and automatically decompress compressed files.
- **Usage**:
  ```dockerfile
  ADD [--chown=<user>:<group>] <src>... <dest>
  ```
- **Example**:
  ```dockerfile
  ADD https://example.com/example.tar.gz /var/www/html/
  ```
- **Notes**: Use `ADD` for remote resources and archives. For all other copying, `COPY` is recommended as it is more transparent.

### WORKDIR
- **Purpose**: Sets the working directory for any `RUN`, `CMD`, `ENTRYPOINT`, `COPY`, and `ADD` instructions that follow in the Dockerfile.
- **Usage**:
  ```dockerfile
  WORKDIR /path/to/workdir
  ```
- **Example**:
  ```dockerfile
  WORKDIR /app
  ```
- **Notes**: If the `WORKDIR` does not exist, it will be created even if it’s not used in any subsequent Dockerfile instruction.



## Managing Dependencies and Packages
### Using RUN for Installation
- **Purpose**: Installs packages using the package manager available in the image.
- **Common Usage**:
  - For Debian/Ubuntu-based containers:
    ```dockerfile
    RUN apt-get update && apt-get install -y package-name
    ```
  - For Red Hat/CentOS-based containers:
    ```dockerfile
    RUN yum install -y package-name
    ```
  - For Alpine-based containers:
    ```dockerfile
    RUN apk add --update package-name
    ```
- **Example**:
  ```dockerfile
  RUN apt-get update && apt-get install -y curl
  ```

### Cleaning Up
- **Purpose**: Reduces the image size by cleaning up unnecessary files and cache.
- **Usage**:
  ```dockerfile
  RUN apt-get install -y package-name \
      && rm -rf /var/lib/apt/lists/*
  ```
- **Example**:
  ```dockerfile
  RUN apt-get update && apt-get install -y \
      git \
      && apt-get clean \
      && rm -rf /var/lib/apt/lists/*
  ```

### Minimizing Layer Count
- **Purpose**: Consolidates RUN commands to reduce the number of layers, thus improving the build process and reducing the image size.
- **Best Practice**:
  - Chain commands using `&&`.
  - Avoid unnecessary layers by combining related tasks into a single `RUN` statement.
- **Example**:
  ```dockerfile
  RUN apt-get update && apt-get install -y \
      curl \
      git \
      && apt-get clean \
      && rm -rf /var/lib/apt/lists/*
  ```

### Using Build Arguments (ARG)
- **Purpose**: Allows you to pass variables during the build stage, which can be used to customize the installation of packages.
- **Usage**:
  ```dockerfile
  ARG VERSION=latest
  RUN apt-get install -y package-name=${VERSION}
  ```
- **Example**:
  ```dockerfile
  ARG PHP_VERSION=7.4
  RUN apt-get update && apt-get install -y \
      php${PHP_VERSION}
  ```
	

## Running Commands and Processes
### CMD
- **Purpose**: Specifies the default command to run when a container starts. Only the last `CMD` instruction in a Dockerfile will take effect.
- **Usage**:
  ```dockerfile
  CMD ["executable","param1","param2"]  # exec form, preferred
  CMD command param1 param2            # shell form
  ```
- **Examples**:
  ```dockerfile
  CMD ["echo", "Hello world"]  # Using exec form
  CMD echo Hello world         # Using shell form
  ```
- **Notes**: If `CMD` is used to provide default command-line arguments for `ENTRYPOINT`, both should be specified in the JSON array format.

### ENTRYPOINT
- **Purpose**: Configures a container to run as an executable. Any `CMD` instructions become default parameters and can be overridden from the command line when the container starts.
- **Usage**:
  ```dockerfile
  ENTRYPOINT ["executable", "param1", "param2"]  # exec form, preferred
  ENTRYPOINT command param1 param2              # shell form
  ```
- **Examples**:
  ```dockerfile
  ENTRYPOINT ["/usr/sbin/apache2ctl", "-D", "FOREGROUND"]
  ENTRYPOINT exec top -b
  ```
- **Notes**: Using the exec form ensures that the executable receives signals intended for it, unlike the shell form where the signal is received by the shell process.

### CMD vs ENTRYPOINT
- **Comparison**: While `CMD` can be seen as a way to define default execution commands and arguments, `ENTRYPOINT` establishes a container with a specific service in mind, allowing the user to append only new arguments and not overwrite the entire command.
- **Best Practice**:
  - Use `ENTRYPOINT` for setting the container's main application.
  - Reserve `CMD` for default arguments and running additional setups before the main process begins.

### Combining CMD and ENTRYPOINT
- **Purpose**: To allow the docker container to be run both as an executable and to allow flexibility with the arguments passed.
- **Example**:
  ```dockerfile
  ENTRYPOINT ["executable", "param1"]
  CMD ["param2", "param3"]
  ```
- **Explanation**: In this configuration, `param1` is a fixed part of the command, while `param2` and `param3` can be overridden when running the container.



## Volumes and Data Management
### VOLUME
- **Purpose**: Creates a mount point with the specified name and marks it as holding externally mounted volumes from the native host or other containers. It’s often used to preserve data across container updates and restarts.
- **Usage**:
  ```dockerfile
  VOLUME ["/data"]
  ```
- **Example**:
  ```dockerfile
  VOLUME /var/log /var/db
  ```
- **Notes**:
  - `VOLUME` can be used to enable access to Docker data from outside the Docker container and to share data between containers.
  - When a volume is declared, any changes made to that volume will be made directly on the host machine and will persist even after the container is deleted.

### Best Practices for Data Management
- **Decouple applications from storage**: Store data (such as database files) on volume containers or mount host directories as volumes.
- **Read-only volumes**: For added security, specify volumes as read-only when sensitive data must not be modified by the container.
- **Example**:
  ```dockerfile
  VOLUME ["/data:ro"]
  ```
- **Temporary file storage**: Consider using volumes for temporary file storage to avoid filling up the container writable layer and causing performance degradation.

### Managing Data in Docker
- **Backup, restore, and migrate data volumes**: To handle data effectively, you can use Docker commands to backup, restore, or migrate volumes from one container to another.
- **Example Commands**:
  - Backup: `docker run --rm --volumes-from dbstore -v $(pwd):/backup ubuntu tar cvf /backup/backup.tar /dbdata`
  - Restore: `docker run --rm --volumes-from dbstore2 -v $(pwd):/backup ubuntu tar xvf /backup/backup.tar`
- **Notes**:
  - Ensure that operations on data volumes do not interrupt running services unless necessary.


## Network Configuration
### EXPOSE
- **Purpose**: Informs Docker that the container listens on the specified network ports at runtime. This is a declaration and does not actually publish the port.
- **Usage**:
  ```dockerfile
  EXPOSE <port> [<port>/<protocol>...]
  ```
- **Example**:
  ```dockerfile
  EXPOSE 80/tcp
  EXPOSE 443
  ```
- **Notes**: 
  - `EXPOSE` does not make the ports of the container accessible to the host. To do this, you need to run the container with the `-p` flag.
  - This instruction is useful for building images that are meant to intercommunicate or are intended to be run in linked containers.

### Setting Default Network Settings
- **Purpose**: Customize network settings such as network mode, enabling IPv6, or using user-defined bridge networks.
- **Usage**:
  - When running containers, use Docker run commands to specify networking configurations:
    ```bash
    docker run --network=host --name container_name image_name
    ```
- **Example**:
  ```bash
    docker run -d --network=my-network --name my-app my-image
  ```
- **Notes**:
  - Common network modes include `bridge`, `host`, `none`, and user-defined networks.
  - `--network=host` uses the host’s networking stack, and not isolated networking for the container.

### Linking Containers
- **Purpose**: Allows containers to communicate with each other without using port mappings, using a private internal network.
- **Usage**:
  - Link two containers:
    ```bash
    docker run --link <name or id>:alias
    ```
- **Example**:
  ```bash
    docker run --name database --detach some-database
    docker run --detach --name app --link database:db my-app-image
  ```
- **Notes**:
  - Linking is a legacy feature and might be removed in future Docker versions. It’s recommended to use user-defined networks to facilitate communication between containers.


## Best Practices
### Minimize the Number of Layers
- **Purpose**: Reduce image size and build complexity by minimizing the number of layers.
- **Practice**: Combine related commands into a single `RUN` statement where possible, and use multi-stage builds to separate parts of the build process that aren't needed in the final image.
- **Example**:
  ```dockerfile
  RUN apt-get update && apt-get install -y \
      git \
      curl \
      && rm -rf /var/lib/apt/lists/*
  ```

### Use .dockerignore
- **Purpose**: Speed up the build process by excluding files and directories that aren't necessary for building the Docker image.
- **Practice**: Create a `.dockerignore` file in the root of your context directory to exclude files like temporary files, logs, and local configuration files.
- **Example**:
  ```
  .git
  node_modules
  tmp/
  ```

### Leverage Build Cache
- **Purpose**: Make builds faster by reusing previously cached layers.
- **Practice**: Structure Dockerfile instructions to maximize cache utilization. For instance, if you're copying files and then running package installations, copy only the files needed for the installation first, perform the installation, then copy the rest of the files.
- **Example**:
  ```dockerfile
  COPY package.json /app/
  RUN npm install
  COPY . /app
  ```

### Use Specific Base Images
- **Purpose**: Enhance security and reduce image sizes by using specific, possibly slimmed-down base images.
- **Practice**: Instead of using generic and large base images like `ubuntu`, use more specific versions like `ubuntu:20.04` or even better, `ubuntu:20.04-slim`.
- **Example**:
  ```dockerfile
  FROM node:14-alpine
  ```

### Avoid Running as Root
- **Purpose**: Improve security by limiting the privileges of container processes.
- **Practice**: Use the `USER` instruction to switch to a non-root user after installing necessary software.
- **Example**:
  ```dockerfile
  RUN adduser -D myuser
  USER myuser
  ```

### Secure Secrets Management
- **Purpose**: Protect sensitive information such as passwords and API keys.
- **Practice**: Avoid hardcoding secrets in Dockerfiles. Use environment variables, Docker secrets, or third-party secrets management tools.
- **Example**:
  ```dockerfile
  ENV API_KEY_ENV_VAR_NAME
  ```
	
	
## Advanced Features
### Multi-stage Builds
- **Purpose**: Simplify the creation of lightweight and secure images by separating build environments from runtime environments.
- **Usage**:
  ```dockerfile
  # Build stage
  FROM golang:1.16 as builder
  WORKDIR /go/src/app
  COPY . .
  RUN go build -o /my-app

  # Final stage
  FROM alpine:latest
  COPY --from=builder /my-app /my-app
  CMD ["/my-app"]
  ```
- **Example**:
  ```dockerfile
  FROM node:12 as builder
  WORKDIR /app
  COPY package*.json ./
  RUN npm install
  COPY . .
  RUN npm run build

  FROM nginx:alpine
  COPY --from=builder /app/dist /usr/share/nginx/html
  ```
- **Notes**: This method is particularly useful for languages and frameworks like Go, Java, or Node.js where building the application requires a different set of dependencies than running it.

### Using ONBUILD
- **Purpose**: Adds a trigger instruction that will be executed at a later time, when the image is used as the base for another build.
- **Usage**:
  ```dockerfile
  ONBUILD ADD . /app/src
  ONBUILD RUN /usr/local/bin/python-build --dir /app/src
  ```
- **Example**:
  ```dockerfile
  FROM python:3.7
  ONBUILD COPY requirements.txt /app/
  ONBUILD RUN pip install --no-cache-dir -r /app/requirements.txt
  ```
- **Notes**: `ONBUILD` is useful for images that are going to be the base of another build, like frameworks or development environments, ensuring that any derived image automatically includes certain necessary instructions.

### Health Checks
- **Purpose**: Allows you to configure the Docker container to periodically check the health of a process or application running within it.
- **Usage**:
  ```dockerfile
  HEALTHCHECK --interval=5m --timeout=3s \
    CMD curl -f http://localhost/ || exit 1
  ```
- **Example**:
  ```dockerfile
  HEALTHCHECK CMD curl --fail http://localhost:8080/health || exit 1
  ```
- **Notes**: Health checks can help identify containers that are running but not actually functional. Docker can restart them automatically depending on the configured restart policy.



## Troubleshooting and Debugging
### Common Issues and Solutions
- **Docker build failures**:
  - **Symptoms**: Build stops with an error message.
  - **Common Causes**: Syntax errors in Dockerfile, missing files in context, permissions issues.
  - **Solution**:
    - Check Dockerfile syntax and ensure all referenced files are available in the build context.
    - Ensure that file permissions allow Docker to access necessary files.

- **Container won't start**:
  - **Symptoms**: Container exits immediately after start or fails to start.
  - **Common Causes**: Misconfiguration in `CMD` or `ENTRYPOINT`, necessary services not started.
  - **Solution**:
    - Use `docker logs container_name` to check the logs for error messages.
    - Verify that `CMD` and `ENTRYPOINT` scripts are executable and correctly formatted.

### Using Docker Logging
- **Purpose**: Logs provide insights into what happens when a container runs.
- **Usage**:
  ```bash
  docker logs [container_id or name]
  ```
- **Example**:
  ```bash
  docker logs my-running-app
  ```
- **Notes**:
  - Checking logs is often the first step in troubleshooting container issues, as they can reveal errors and other runtime information.

### Monitoring Tools
- **Purpose**: Monitoring tools help track container performance and health.
- **Common Tools**:
  - **Docker Stats**: Provides a live stream of container resource usage statistics.
    ```bash
    docker stats
    ```
  - **Portainer**: A GUI for managing Docker environments.
  - **cAdvisor**: Google's container advisor that provides container users an understanding of the resource usage and performance characteristics of their running containers.

### Debugging Best Practices
- **Reproducibility**: Ensure that the error can be consistently reproduced to accurately diagnose the issue.
- **Isolation**: Isolate the problematic part of your Dockerfile or container configuration to identify the specific cause.
- **Incremental Changes**: Make one change at a time to your Dockerfile or container configuration to see what affects the behavior.


## Resources
### Official Docker Documentation
- **Purpose**: Provides comprehensive and authoritative details on all aspects of Docker.
- **Link**:
  - [Docker Official Documentation](https://docs.docker.com)

### Recommended Books
- **Docker Deep Dive** by Nigel Poulton
  - **Overview**: This book is great for both beginners and seasoned users. It covers fundamental concepts to advanced topics in Docker.
- **Docker Up & Running** by Sean Kane and Karl Matthias
  - **Overview**: Explores practical use cases and best practices for deploying Docker containers at scale.

### Online Courses
- **Docker Mastery: with Kubernetes +Swarm from a Docker Captain** on Udemy
  - **Overview**: A comprehensive course that not only covers Docker but also includes Kubernetes and Swarm, making it ideal for those looking to expand beyond basic Docker usage.
- **Introduction to Docker** on Coursera
  - **Overview**: Focuses on the basics and is offered by Duke University, making it a solid foundation course.

### Video Tutorials
- **Docker Official YouTube Channel**
  - **Link**:
    - [Docker YouTube Channel](https://www.youtube.com/docker)
  - **Content**: Offers a range of tutorials, talks, and demos to help you understand Docker from the ground up.

### Community and Forums
- **Docker Community Slack**
  - **Link**:
    - [Join Docker Slack](https://www.docker.com/docker-community)
  - **Purpose**: Connect with Docker experts and enthusiasts around the world to share knowledge and solve problems.
- **Stack Overflow**
  - **Tag**:
    - [Docker Questions on Stack Overflow](https://stackoverflow.com/questions/tagged/docker)
  - **Purpose**: A great place to find solutions to specific problems and engage with an active community of developers.
