# Microservice-Kubernetes
Kubernetes to deploy a Microservice architecture. I'll deploy, manage and monitor a live Kubernetes cluster.

## Technologies: Event Driven Arcitecture
- Java
- ActiveMQ
- Angular(Javascript Framework)

## Install Kubernetes
- Go to this url and follow the installation instruction: https://kubernetes.io/docs/tasks/tools/install-minikube/

- After Installation run the command to check if it's installed: `minikube` on the terminal
- Run `minikube start`
- Run `minkube status`

## Test Minikube environment variables
- RUN: `minkube docker-env`

```
export DOCKER_TLS_VERIFY="1"
export DOCKER_HOST="tcp://192.168.49.2:2376" 
export DOCKER_CERT_PATH="/home/foldername/.minikube/certs"
export MINIKUBE_ACTIVE_DOCKERD="minikube"
```

## To point your shell to minikube's docker-daemon:
- RUN: `eval $(minikube -p minikube docker-env)`

## Now RUN: this enables docker and Kubernetes to use less resources
- `docker image ls`




## Fleet Management System using Kubernetes
- The backend is developed in Java
- The frontend is developed using Angular


## Get the IP of the Kubernetes Instance
- Locally run `minikube ip`

## Check the Pod detail: podName
- RUN `kubectl describe pod webapp`

## Execute a command on a pod: kubectl exec podName commandName
- RUN `kubectl exec webapp ls`

- RUN `kubectl -t exec webapp sh` 

