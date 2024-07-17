kubectl run --image=nginx custom-nginx --port=8080

kubectl scale deployment webapp --replicas=3

kubectl create deployment --image=kodekloud/webapp-color webapp

kubectl create service clusterip redis-service --tcp=6379:6379

kubectl create deployment --image=redis --namespace=dev-ns redis-deploy

kubectl config set-context --current --namespace=dev-ns

kubectl scale deployment redis-deploy --replicas=2

kubectl expose pod httpd --port=8080 --target-port=80 --typ
e=ClusterIP

kubectl expose --help