# Sock Shop : A Microservice Demo Application
This is an installation guide for deploying SockShop using Docker Compose. For our experiment, we reused images created by [Lilly Wu](https://hub.docker.com/r/lillywu/sock-shop/tags), which slightly modified the original images to accommodate stress-ng.
## Pre-requisites
- Docker
- Docker-Compose
## Clone the microservices-demo repo
```
git clone https://github.com/vuDevOps/microservices-demo
cd microservices-demo
```
## Deploying Sock Shop
While being within the `microservices-demo` folder, ou can deploy all Sock Shop services using the following docker compose command:
```
docker compose -f deploy/docker-compose/docker-compose.yml up -d
```
## Deploy monitoring tools
Additionally, you can deploy monitoring tools such as Prometheus and Grafana, to monitor metrics for Sock Shop, using the following command:
```
docker compose -f deploy/docker-compose/docker-compose.monitoring.yml up -d
```

## Access Sock Shop

Once the application is deployed, navigate to http://localhost:8080 to access the Sock Shop home page.

The Prometheus dashboard is available at http://localhost:30000.

The Grafana dashboard is available at http://localhost:30001.

## Undeploy Sock Shop
```
docker compose -f deploy/docker-compose/docker-compose.yml down

docker compose -f deploy/docker-compose/docker-compose.monitoring.yml down
```
