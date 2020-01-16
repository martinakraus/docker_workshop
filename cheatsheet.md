# Docker command CheatSheet


## Images 

### Listing the Docker Images
`$ docker images`

### Filtering

`docker images --filter=reference='alpine'`

### Remove all images

List:

`docker images -a`

Remove:

`docker rmi $(docker images -a -q)`


## Containers

### Listing Containers
`$ docker ps (-a)`

### Remove all exited containers

List:

`docker ps -a -f status=exited`

Remove:

`docker rm $(docker ps -a -f status=exited -q)`
