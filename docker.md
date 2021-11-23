# DOCKER

### Display list of existing containers already built on hard disk
> docker ps --all

### Display list of running containers on hard disk
> docker ps

### docker run = docker create + docker start
> docker run = docker create + docker start
>
> docker create {container_name}
>
> docker start {container_id}
>
### -a -> display the output
> docker start -a <id>

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
- -i stands for execute new command inside the container
- -t stands for prettify
> docker exec -it {container_id} {command}
> > docker run redis
> >
> > docker exec -it {container_id} redis-cli