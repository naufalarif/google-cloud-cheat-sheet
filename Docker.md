Build Image
docker build --tag IMAGE_NAME
if you don't provide --tag, doocker automatically set it to latest

Check Image
docker images

Remove Image
docker rmi IMAGE_ID
or
docker rmi IMAGE_NAME

Run Image as Container
docker run -p HOST_PORT:CONTAINE_PORT IMAGE_NAME

Check Container
docker ps

Remove Container
docker rm CONTAINER_NAME

Stop Container
docker stop CONTAINER_NAME
