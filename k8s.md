# KUBERNETES
> an open-source system for automating deployment, scaling, and management of containerized applications"



[youtube](https://youtu.be/wHha-Q3XVOg)

> ### CREATE ALIAS TO TYPE FASTER
> - alias k=kubectl

> ### CREATE A NEW NAMESPACE TO WORK FROM
> - k create ns task
> - k get ns

> ### SET THE CONTEXT & THE CURRENT NAMESPACE TO THE ONE THAT WE JUST CREATED
> it just allows us to not have tp type namespace everytime we type in command
> - k config set-context --current --namespace=task

> ### CREATE A FILE
> - printf "Hello, World!" > value.txt

> ### CREATE A CONFIGMAP 
> with a variable called "greeting" with a value pointing to the file previously created
> - k create cm task-cm --from-file=greeting=value.txt -n task
> - k get cm
> - k describe cm task-cm

> ### CREATE A NEW DEPLOYMENT
> BusyBox deployment with 5 replicas and expose the config map variable greeting as an environment variable called "MY_GREETING"
> 
> Pass the command 'env' to the running containers and stop each of the containers from exiting
> - k create deployment task-deployment --image=busybox -n task --replicas=5 --dry-run=client -o yaml > task-deployment.yml