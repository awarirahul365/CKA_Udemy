# Encode CSR
cat akshay.csr | base64 -w 0

# Get CSR

kubectl get csr

# Edit CSR

kubectl edit csr agent-smith

# Approve or deny certificate 

kubectl certificate deny agent-smith

https://kubernetes.io/docs/reference/access-authn-authz/certificate-signing-requests/

# Create client certificates

generate the keys 
openssl genrsa -out ca.key 2048

sign the certificates
openssl req -new -key ca.key -subj "/CN=KUBERNETES-CA" -out ca.csr

sign the certificates
openssl x509 -req -in ca.csr -signkey ca.key -out ca.crt