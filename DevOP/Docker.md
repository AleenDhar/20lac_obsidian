# basics
```cli
docker run -v

docker run -it ubuntu

docker run -it node
```

```
docker start <name/id of the container>
docker stop <noc>

docker exec -it <name/id of the container> bash

#stupid commands
docker exec <id of the container> ls
```
# port mapping
```
docker run -it -p <main device port>:<docker port> <container name/id>
```

# docker file

docker build command:
```
docker build -t <name> .
```

```Dockerfile
FROM 
```
