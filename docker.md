# DOCKER

### Display list of existing containers already built on hard disk
> docker ps -a

### Display list of running containers on hard disk
> docker ps

### Try to create and start the container
> docker run = docker create + docker start
>
> docker create {image_name}
>
> docker start {container_id}

### Display the output
> #### use -a
> > docker start -a {container_id}

### Running on the background
> #### use -d
> > docker run -d {image-name}

### Specify the file that we are going to use
> docker build -f {custom_file_name} .

### Port Mapping
> docker run -p {local_port}:{container_port} {image_name}

### Volume Mapping
> mount the external directory to a folder inside the docker container
> > docker run -v {local_directory}:{container_directory} {image_name}

### Remove a container
> docker rm {container_id}
>
> docker rm {container_name}

### Remove images
> Notes : Remember to ensure that no containers are running off that image before attempting to remove the image
> You must stop and delete all the dependent containers to be able to delete an image
> > docker rmi {image_name}
> >
> > docker rm {image_id}

### Delete all the containers and cache
> hendrik@LAPTOP-6TGTH85J:/mnt/c/Users/Hendrik$ docker system prune
>
> WARNING! This will remove:
> - all stopped containers
> - all networks not used by at least one container
> - all dangling images
> - all dangling build cache
>
> Are you sure you want to continue? [y/N]

### docker stop & docker kill
> #### use SIGTERM
> will wait for 10 seconds to terminate the id
> > docker stop {container_id}
>
> #### use SIGKILL
> > docker kill {container_id}

### Multi command container
Execute an additional command in a container
- -i stands for interactive (execute new command inside the container)
- -t stands for terminal (prettify)
> docker exec -it {container_id} {command}
> > docker run redis
> >
> > docker exec -it {container_id} redis-cli

### Tagging the image
> docker tag {image_id} {custom_image_name}

### Tagging the image during build
> #### use -t
> > docker build -t {custom_image_name} .

### Compose
> docker compose up
>
> docker compose down