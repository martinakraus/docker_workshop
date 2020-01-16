# Managing Docker containers

## Preparations

 - Clean your docker host using the commands (in bash):

```
$ docker rm -f $(docker ps -a -q)
```

## Instructions

 - Run the following container from the dockerhub:
```
$ docker run -d -p 8080:8080 --name app1 codekittey/cat-web
```

 - Ensure the containers are running:
```
$ docker ps
```

 - Run a second container with same image:
```
$ docker run -d -p 8081:8080 --name app2 codekittey/cat-web
```

 - Display running containers:
```
$ docker ps
```

 - Show all the containers (including non running containers):
```
$ docker ps -a
```

 - Restart the second container:
```
$ docker restart app2
```

 - Display the docker host information with:
```
$ docker info
```

 - Show the running processes in the first container using:
```
$ docker top app1
```

 - Retrieve the history of the second container:
```
$ docker history selaworkshops/python-app:2.0
```

 - Inspect the first container and look for the internal ip:
```
$ docker inspect app1
```
```
"Networks": {
                "bridge": {
                    "IPAMConfig": null,
                    "Links": null,
                    "Aliases": null,
                    "NetworkID": "822cb66790c6358d9decab874916120f3bdeff7193a4375c94ca54d50832303d",
                    "EndpointID": "9aa96dc29be08eddc6d8f429ebecd2285c064fda288681a3611812413cbdfc1f",
                    "Gateway": "172.17.0.1",
                    "IPAddress": "172.17.0.3",
                    "IPPrefixLen": 16,
                    "IPv6Gateway": "",
                    "GlobalIPv6Address": "",
                    "GlobalIPv6PrefixLen": 0,
                    "MacAddress": "02:42:ac:11:00:03",
                    "DriverOpts": null
                }
            }
```

 - Show the logs of the second container using the flag --follow:
```
$ docker logs --follow app2
```

 - Browse to the application and see the containers logs from the terminal:
```
http://localhost:8081
```

 - Stop to tracking logs:
 ```
$ CTRL + C
```
