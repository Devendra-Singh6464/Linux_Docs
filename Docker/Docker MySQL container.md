*First of all to docker installed on your server*
* Pull the mysql image to following links
* https://hub.docker.com/_/mysql ,
* https://hub.docker.com/r/mysql/mysql-server/ ,
* https://dev.mysql.com/doc/mysql-installation-excerpt/8.0/en/docker-mysql-getting-started.html#docker-download-image

* Create MYSQL docker container.
``` shell
docker run --name mysql-test -p 3306:3307 -e MYSQL_ROOT_PASSWORD=webkul -d mysql-container
``` 
- **Pull docker mysql image and run mysql container.**  
   `Syntax`: `Docker run --name <your_container_name_you_want_to_set> -p<port> <host-machine>:<container> -e MYSQL_ROOT_PASSWORD=<Set_database_login_password> -d <mysql_docker_image_name>`
*3306: host-machine port
3307: container port*

``` shell
docker exec -it test-mysql /bin/bash
```
`docker exec `: Runs a command inside a running container.
`-it`: Combines two options:
`-i`: Keeps the session interactive (so you can type commands).
`-t`: Allocates a terminal (like a shell).
`test-mysql`: This is the name of the running container where you want to run the command.
`/bin/bash`: The command to run inside the container (here, it's opening the bash shell).

- This command opens a `bash shell` inside the `test-mysql` container, allowing you to interact with it.
- If the container doesn't have bash installed, you might want to try `/bin/sh` instead:

### Docker Volumes

A Docker volume is a persistent storage mechanism that allows data to be stored outside of a Docker container. By default, any data created or changed inside a container is lost when the container stops or is removed. A volume ensures that data survives container restarts and deletions.

Think of it as a place where you can save files that need to persist, even if the container stops or is recreated.

_Key Points:_

1. Volumes are independent of containers.
2. Volumes can be shared between containers.
3. Volumes help you persist data, like database files, even if the container is deleted.

_Create a Docker Volume_

- Syntax  
    To mount a volume with the docker run command, you can use either the `--mount` or `--volume` flag.

```shell
docker run --mount type=volume,src=<volume-name>,dst=<mount-path>
docker run --volume <volume-name>:<mount-path>
```

In general, `--mount` is preferred. The main difference is that the `--mount` flag is more explicit and supports all the available options.

- List all volumes.
```shell
docker volume ls
```

- Remove docker volume
```shell
docker volume rm mysql-data
```

- All volumes are managed by Docker and stored in a dedicated directory on your host, usually `/var/lib/docker/volumes` for Linux systems.


*To access the old MySQL data in the new MySQL container after you've deleted the previous container but retained the Docker volume, you need to ensure that the new container is using the same volume where the old MySQL data was stored.*
- you can look at the volumes in your Docker installation:
``` shell 
docker volume ls
```

You can also check the exact mount point of the volume in `/var/lib/docker/volumes/` to confirm the correct volume. If you know the volume name (for example `mysql-test`), you can check its path.
``` shell
ls /var/lib/docker/volumes/mysql-test/_data
```
- Run the New MySQL Container Using the Same Volume.
``` shell
docker run --name mysql-new-container -p 3306:3306 -e MYSQL_ROOT_PASSWORD=webkul -v mysql-test:/var/lib/mysql -d mysql
```

*docker volume add on mysql container.*
``` shell
docker run -d -p 3306:3307 -v mysql-test-mysql-data:/var/lib/mysql --name mysql-test-new mysql:latest
```

Name: "mysql-test-mysql-data"
This is the name of the storage box (volume). It's like libelling your box "mysql-test-mysql-data" to keep track of it.

**How to Enable Automatic Start of Docker Container:**
Use `--restart` always or `--restart unless-stopped` to ensure the container restarts on boot:

Example 1: Start a container with always restart policy:
``` shell
docker run -d --name my-container --restart always my-image
```

This command will run the container in detached mode (-d) and ensure that the container always restarts when the system reboots.

Example 2: Start a container with unless-stopped restart policy:
``` shell 
docker run -d --name my-container --restart unless-stopped my-image
```

With this policy, the container will restart on reboot unless you explicitly stop it with docker stop my-container.

If the container is already running, you can update the restart policy using docker update:
``` shell 
docker update --restart always my-container
```

This command updates the restart policy for an existing container (my-container) to always restart when the system reboots.

Verify Restart Policy: To verify the restart policy of a running container, use the following command
``` shell 
docker inspect --format '{{.HostConfig.RestartPolicy.Name}}' my-container
```

This will return the restart policy of the container (e.g., always, unless-stopped, etc.).
- Stop, remove all the container
```shell
docker stop/rm -a
```

