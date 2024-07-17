# Command to get all pods name with namespaces

kubectl get pods -A

# Command to delete pods 

kubectl delete pods --all -n <namespace>

kubectl delete pod <pod-name>

kubectl delete pods -l app=<app-name>

# Command to create nginx server

kubectl run nginx --image nginx

# Create Pods using Yaml

kubectl create -f pods_create.yml

# Description of Pods

kubectl describe pod myapp-pod

# Edit Command 

kubectl edit pod <pod name>
