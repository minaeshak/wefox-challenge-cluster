# Wefox Challenge Cluster

## First: Setting Up Minikube cluster and Kubectl installation

1. Minikube installation : https://minikube.sigs.k8s.io/docs/start/
2. Kubectl installation: https://kubernetes.io/docs/tasks/tools/install-kubectl-linux/

## Second: Running deploy.sh script 
By running this script it will start minikube cluster which is named wefox-challenge-hello then it will deploy the kubernetes Pod and NodePort Service.
After that minikube cluster IP is fetched to be mapped in the /etc/hosts file for create local domain name
Please check example.png file as the output should be like this

## Cluster Enhancement Plan
As this is a Pre-Prod Cluster , When can then setup the cluster on one of the cloud providers like AWS EKS or Google Kubernetes Engine.
In such case we will add ingress controller and loadbalancer service for achieving high availability.

## Deploying version 0.2.1 and then 0.2.3
In this example we deployed simple pod for our application for scaling and flexiblity in changing image tag we can create deployment and use this pod as a template.
Hence, it will be easily changing the image version using the strategy specified like rolling updates
