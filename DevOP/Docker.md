# basics

used to run images
```cli
docker run -v

docker run -it ubuntu

docker run -it node
```

used for the containers
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
  

FROM ubuntu:latest

RUN apt-get update && apt-get install -y curl

RUN curl -sL https://deb.nodesource.com/setup_18.x | bash -

RUN apt-get update -y

RUN apt-get install -y nodejs

COPY . /home/app

WORKDIR /home/app

RUN npm install

  

EXPOSE 5000

  

ENTRYPOINT [ "node","index" ] #CMD ["node","index"]
```
# docker-compose.yml

running docker-compose
```
docker compose up
```

docker-compose.yml
```
version:'3.8'

version: '3.8'
services:
  postgres: # name
    image: postgres # hub.docker.com
    ports:
      - "5432:5432"
    environment:
      POSTGRES_USER: postgres
      POSTGRES_DB: review
      POSTGRES_PASSWORD: password
  redis: # name
    image: redis
    ports:
      - "6379:6379"

```