# Docker_Python

Here we will build a docker image for the above python server, containerize it and then upload it on to dockerhub.

## Login to Dockerhub

Run ```docker login``` and enter your credentials.

## Build the image

Run ```docker build -t python-http-server .``` in the repositories directory. This will build the image for the python server.

## Containerize the image

Run ```docker run -d -p 8080:8080 --name ilyas python-http-server``` to containrize the image.

## Upload the container to Dockerhub

Run the following commands to upload on to dockerhub:

```docker run -d -p 5000:5000 registry```

```docker tag python-http-server docker.io/ilyashusain/python-server```

```docker push ilyashusain/python-server```
