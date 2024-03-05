running redis-stack on docker(port 8001 is for the gui)
```
docker run -d --name redis-stack -p 6379:6379 -p 8001:8001 redis/redis-stack:latest
```