# Basic microservices environment

This is a simple environment to serve as an example of how microservices are built and how they work and communicate inside a network.

## Start the project

After cloning the main repo you need to clone the submodules
(the `--init` flag is only used the first time)

```
git submodule update --init --recursive
```

Then just type the command

```
docker-compose up
```

This will start the construction of the Docker images of every module inside the poyect (This may take a wile) in a multi step build that consist of copying the source code to a container to build the jar with gradle and then use the resulting jar to create an image for the microservice, the image used to start a container.

After that is a matter of time to let the API gateway and service registry to get up and running, exposing the other services.

## Service Endpoints

### Eureka

http://localhost:8761/

### Clients MS

http://localhost:8101/clients/api/swagger-ui/

### Data ms

http://localhost:8101/data/swagger-ui/
