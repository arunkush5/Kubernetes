# Kubernetes
kubctl Pack

# Get all pods in the current namespace
kubectl get pods

# Get pods in all namespaces
kubectl get pods --all-namespaces

# Get pods with more details 
kubectl get pods -o wide

# Get the yaml for a pod
kubectl get pod <pod> -o yaml

# Inspect a pod
kubectl describe pods <pod>

# Get pods sorted by a metric
kubectl get pods \
  --sort-by='.status.containerStatuses[0].restartCount'

# Get pods with their labels
kubectl get pods --show-labels

# Get pods that match a label
kubectl get pods -l <label>=<value>

# Forward traffic from a localhost port to a pod port
kubectl port-forward <pod> <localhost-port>:<pod-port>

# Run a command on a pod
kubectl exec <pod> -- <command>

# Run a command on a container in a pod
kubectl exec <pod> -c <container> -- <command>
