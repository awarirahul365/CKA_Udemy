kubectl create secret generic db-secret --from-literal=DB_HOST=sql01 --from-literal DB_User=root --from-literal DB_Password=password123

kubectl describe secret db-secret

echo -n "mysql" | base64 --decode


Name:         db-secret
Namespace:    default
Labels:       <none>
Annotations:  <none>

Type:  Opaque

Data
====
DB_HOST:      5 bytes
DB_Password:  11 bytes
DB_User:      4 bytes

