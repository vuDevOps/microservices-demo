# Sock Shop : A Microservice Demo Application
## Updated: Installation Guide
## Pre-requisites
- Install Minikube
- Install kubectl
## Clone the microservices-demo repo
```
git clone https://github.com/vuDevOps/microservices-demo
cd microservices-demo
```
## Start Minikube
You can start Minikube by running:
```
minikube start --memory 8192 --cpus 4
```
## Deploy Sock Shop
Deploy the Sock Shop application on Minikube
```
kubectl create -f deploy/kubernetes/manifests/00-sock-shop-ns.yaml -f deploy/kubernetes/manifests
```
To start Opentracing run the following command after deploying the sock shop
```
kubectl apply -f deploy/kubernetes/manifests-zipkin/zipkin-ns.yaml -f deploy/kubernetes/manifests-zipkin
```
Wait for all the Sock Shop services to start:
```
kubectl get pods --namespace="sock-shop
```
## Check the Sock Shop webpage

Once the application is deployed, navigate to http://192.168.99.100:30001 to see the Sock Shop home page