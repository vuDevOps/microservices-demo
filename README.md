# Sock Shop : A Microservice Demo Application
This is an installation guide for deploying SockShop using Docker Compose. For our experiment, we reused images created by [Lilly Wu](https://hub.docker.com/r/lillywu/sock-shop/tags), which slightly modified the original images to accommodate stress-ng.
## Pre-requisites
- Install Docker
## Clone the microservices-demo repo
```
git clone https://github.com/vuDevOps/microservices-demo
cd microservices-demo
```
## Deploying Sock Shop
You can deploy all sock shop serivices using the following docker compose command:
```
docker compose -f deploy/docker-compose/docker-compose.yml up -d
```
## Deploy monitoring tools
In addition to the Sock Shop you can deploy monitoring tools such as Prometheus and Grafana using the following command:
```
docker compose -f deploy/docker-compose/docker-compose.monitoring.yml up -d
```

## Check the Sock Shop webpage

Once the application is deployed, navigate to http://localhost:8080 to see the Sock Shop home page

Prometheus is available at http://localhost:30000

Grafana is available at http://localhost:30001

## Undeploy Sock Shop
```
docker compose -f deploy/docker-compose/docker-compose.yml down

docker compose -f deploy/docker-compose/docker-compose.monitoring.yml down
```
