# Docker commands

## Build Docker Image

``` docker build --tag python-docker . ```

## View Docker images

``` docker images ```


## Run docker images as a container

### syntax

-d = detached or running in background
-p = port number

``` docker run -d -p <local-port>:<container-port> <docker-image-name>```

### Example command to run this flask app

``` docker run -d -p 5000:5000 python-docker ```


## See running containers or processes

``` docker ps ```

## See all running containers or processes

``` docker ps -a ```

## Stop running container

``` docker stop <container-name> ```

## Remove docker image

``` docker rmi <image-name> ```

## Remove docker container

``` docker rm <container-name-1> <container-name-2> <container-name-3>```

## Remove unused resources or containers

``` docker container prune ``` 


## Tag images

``` docker tag python-docker:latest python-docker:v1.0.0 ```

## Go into a container

``` docker exec -it <container-name> bash ```



# WSGI Production Server for flask

```
pip install waitress


waitress-serve --port=8080 --call app:index

```