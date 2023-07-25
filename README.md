# Microservice-Kubernetes
Kubernetes to deploy a Microservice architecture. I'll deploy, manage and monitor a live Kubernetes cluster.

## Technologies: Event Driven Arcitecture
- Java
- ActiveMQ
- Angular(Javascript Framework)

## Install Kubernetes for Local testing Purposes
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
Locally run to get the Minikube Address(K8)
- `minikube ip`

## Check the Pod detail: podName RUN:
- `kubectl describe pod webapp`

## Execute a command on a pod: kubectl exec podName commandName
- `kubectl exec webapp ls`

- `kubectl -t exec webapp sh` 

### RUN: Shows services within K8
- `kubectl describe service fleetman-webapp`
- `kubectl describe svc fleetman-webapp` 
### RUN: Show pods with K8 Cluster
- `kubectl get po`
- `kubectl get pods`
- `kubectl get po --show-labels`
### Filtering by release
- `kubectl get po --show-labels -1 release=0` - 

### NOTE:
- In a Cluster each of the Nodes would have been given a security group
- Security Group: is really a firewall. It's Configuration in AWS for any EC2 Instance I can limit the incoming traffic that Node to a specified range of port.

## Helm Charts | Package manager for K8

- To install Helm: 
Go to [Helm](https://helm.sh/docs/intro/quickstart/ "Helm Docs") 
```
curl https://baltocdn.com/helm/signing.asc | gpg --dearmor | sudo tee /usr/share/keyrings/helm.gpg > /dev/null
sudo apt-get install apt-transport-https --yes
echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/helm.gpg] https://baltocdn.com/helm/stable/debian/ all main" | sudo tee /etc/apt/sources.list.d/helm-stable-debian.list
sudo apt-get update
sudo apt-get install helm
```

### To Install the ELK Stack using Helm chart:
Go to [ELK Stack using Prometheus, Fluentd/LogStash & Grafana](github.com/grafana/helm-charts/blob/main/charts/grafana/README.md)