# Procedure :

## Source
https://www.youtube.com/watch?v=s_o8dwzRlu4

## Start minikube
minikube start

## Deploy pods
kubectl apply -f .\mongo-config.yaml
kubectl apply -f .\mongo-secret.yaml
kubectl apply -f .\mongo.yaml
kubectl apply -f .\webapp.yaml

## Expose webapp
minikube service webapp-service --url