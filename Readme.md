minikube start -p wefox-challenge-cluster --extra-config=apiserver.service-node-port-range=1-65535
kubectl apply -f http-echo-svc.yaml -f http-echo-pod.yaml 
minikube -p wefox-challenge-cluster service http-echo-svc --url
minikube -p wefox-challenge-cluster ip
echo "$(minikube -p wefox-challenge-cluster ip) hello.wefox.localhost" > /tmp/ip.txt
sudo su - -c "cat /tmp/ip.txt >> /etc/hosts"