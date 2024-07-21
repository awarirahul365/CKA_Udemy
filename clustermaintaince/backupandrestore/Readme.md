export ETCDCTL_API=3

# Take snapshot of ETCDCTL
etcdctl snapshot save --endpoints=127.0.0.1:2379 --cacert=/etc/kubernetes/pki/etcd/ca.crt --cert=/etc/kubernetes/pki/etcd/server.crt --key=/etc/kubernetes/pki/etcd/server.key /opt/snapshot-pre-boot.db

# Restore snapshot of etcd
etcdctl snapshot restore /opt/snapshot-pre-boot.db

# all files are located in
 /etc/kubernetes/manifests

# certificates and variable files

/var/lib/etcd