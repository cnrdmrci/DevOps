# Kubernetes

## Install minikube
```bash
brew install minikube
minikube start
```

## Add image to k8s
```bash
minikube image load my_image
```

## Deployment
```bash
kubectl create deployment hello-minikube --image=k8s.gcr.io/echoserver:1.4
kubectl apply -f deployment.yaml
```

## Service
```bash
kubectl expose deployment hello-minikube --type=NodePort --port=8080
kubectl apply -f service.yaml
```

## Port Forwarding
```bash
kubectl port-forward service/hello-minikube 7080:8080
```

## Ingress
```bash
minikube addons enable ingress
kubectl apply -f ingress.yaml
```

- You can add dns in /etc/hosts for minikube ip
