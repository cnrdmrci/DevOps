# Kubernetes Commands

## K8s Components

```bash 
kubectl get nodes 
```

```bash 
kubectl get pods 
```

```bash 
kubectl get deployments 
```

```bash 
kubectl get services 
```

```bash 
kubectl get replicasets 
```

## CRUD

- Create Deployment

```bash
kubectl create deployment hello-minikube --image=k8s.gcr.io/echoserver:1.4
```

- Edit Deployment

```bash
kubectl edit deployment hello-minikube
```

- Delete Deployment

```bash
kubectl delete deployment hello-minikube
```

- Create, Update Yaml

```bash
kubectl apply -f [yamlFile]
```

- Delete Yaml

```bash
kubectl delete -f [yamlFile]
```

## Pod Log

```bash
kubectl logs [pod-name]
```

## Info Pod

```bash
kbuectl describe pod [pod-name]
```

# Pod Terminal

```bash
kubectl exec -it [pod-name] -- /bin/bash
```

