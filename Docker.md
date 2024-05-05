# Docker Cheat Sheet

### Build Image
```bash
docker build --tag IMAGE_NAME
```

if you don't provide --tag, docker automatically set it to latest

### Check Image
```bash
docker images
```

### Remove Image
```bash
docker rmi IMAGE_ID
```

or
```bash
docker rmi IMAGE_NAME
```

### Run Image as Container
```bash
docker run -p HOST_PORT:CONTAINE_PORT IMAGE_NAME
```

### Check Container
```bash
docker ps
```

### Remove Container
```bash
docker rm CONTAINER_NAME
```

### Stop Container
```bash
docker stop CONTAINER_NAME
```
