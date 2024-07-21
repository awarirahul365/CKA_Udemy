etcd
      --advertise-client-urls=https://192.31.250.3:2379
      --cert-file=/etc/kubernetes/pki/etcd/server.crt
      --client-cert-auth=true
      --data-dir=/var/lib/etcd
      --experimental-initial-corrupt-check=true
      --initial-advertise-peer-urls=https://192.31.250.3:2380
      --initial-cluster=cluster1-controlplane=https://192.31.250.3:2380
      --key-file=/etc/kubernetes/pki/etcd/server.key
      --listen-client-urls=https://127.0.0.1:2379,https://192.31.250.3:2379
      --listen-metrics-urls=http://127.0.0.1:2381
      --listen-peer-urls=https://192.31.250.3:2380
      --name=cluster1-controlplane
      --peer-cert-file=/etc/kubernetes/pki/etcd/peer.crt
      --peer-client-cert-auth=true
      --peer-key-file=/etc/kubernetes/pki/etcd/peer.key
      --peer-trusted-ca-file=/etc/kubernetes/pki/etcd/ca.crt
      --snapshot-count=10000
      --trusted-ca-file=/etc/kubernetes/pki/etcd/ca.crt

# For multi cluster , switch to respective cluster 

kubectl config set-context cluster2

# Get count of cluster 

kubectl config get-context

# If Etcd is external then check through kubeapi server

kubectl describe node kubeapi-server -n=kube-system

# Save ETcd for stacked database

etcdctl snapshot save --endpoints=192.31.250.3:2379 --cacert=/etc/kubernetes/pki/etcd/ca.crt --cert=/etc/kubernetes/pki/etcd/server.crt --key=/etc/kubernetes/pki/etcd/server.key /opt/cluster1.db

# Copy files from cluster to node 

scp cluster1-controlplane:/opt/cluster1.db /opt