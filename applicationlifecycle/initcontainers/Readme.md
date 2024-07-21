Init Containers:
  init-myservice:
    Container ID:  containerd://1b4dc9fc7eb4c75cff605d7ab373ae12baf78a1b05bc2f0b3c805370f42e4a9b
    Image:         busybox
    Image ID:      docker.io/library/busybox@sha256:9ae97d36d26566ff84e8893c64a6dc4fe8ca6d1144bf5b87b2b85a32def253c7
    Port:          <none>
    Host Port:     <none>
    Command:
      sh
      -c
      sleep 5
    State:          Terminated
      Reason:       Completed
      Exit Code:    0
      Started:      Fri, 19 Jul 2024 06:31:07 +0000
      Finished:     Fri, 19 Jul 2024 06:31:12 +0000
    Ready:          True
    Restart Count:  0
    Environment:    <none>
    Mounts:
      /var/run/secrets/kubernetes.io/serviceaccount from kube-api-access-zd4qm (ro)