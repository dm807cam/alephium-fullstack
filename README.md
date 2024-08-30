# Start

```
export HOST_IP=$(hostname -I | awk '{print $1}') && docker-compose up -d
```

Node Swagger: http://127.0.0.1:12973/docs

Explorer Swagger: http://127.0.0.1:9090/docs

Explorer frontend: http://127.0.0.1:3000

# Stop

```
docker-compose down
```
