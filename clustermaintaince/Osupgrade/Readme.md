OS Down for maintain

kubectl drain node01 --ignore-daemonsets --force

kubectl get pods -o wide -n=default

kubectl get pods -o wide

kubectl cordon node01 # makes node unscheduleable

kubectl uncordon node01 # Back to scheduleable

