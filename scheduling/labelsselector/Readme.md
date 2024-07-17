kubectl get pods --selector bu=finance

# Command for all object type that could be present.
kubectl get all --selector env=prod 

kubectl get pod --selector env=prod,bu=finance,tier=frontend