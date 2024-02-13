## Kubernetes Cluster Information 
ssh -p 333 demouser@srecops.com 
user4321

### setup export file 
export KUBECONFIG=/Users/demouser/demo-kubeconfig.yaml

#### Perform excercises 
- Creating a pod with Ubuntu COntainer
```bash
apiVersion: v1
kind: Pod
metadata:
  name: ubuntu-pod
spec:
  containers:
  - name: ubuntu-container
    image: ubuntu
    command: ["sleep"]
    args: ["3600"]

```
This configuration creates a pod named ubuntu-pod with a single container named ubuntu-container, using the ubuntu image from Docker Hub. The container will execute the sleep command with an argument of 3600 seconds (1 hour) to keep it running.

- Create a pod

```bash
kubectl apply -f ubuntu-pod.yaml
```

- Verify the Pod is running
```bash
kubectl get pods
```

- Logging into the Ubuntu Container

```bash
kubectl exec -it <complete pod name> -- /bin/bash
```

- Interacting with the Container
```bash
ls
apt-get-update

try to install netapp cli package or some other package.

```


