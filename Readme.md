# Wefox Challenge Cluster

## First: Setting Up Minikube cluster and Kubectl installation

### 1. Minikube installation : https://minikube.sigs.k8s.io/docs/start/
### 2. Kubectl installation: https://kubernetes.io/docs/tasks/tools/install-kubectl-linux/

## Second: Running deploy.sh script 
By running this script it will start minikube cluster which is named wefox-challenge-hello then it will deploy the kubernetes Pod and NodePort Service.
After that minikube cluster IP is fetched to be mapped in the /etc/hosts file for create local domain name

