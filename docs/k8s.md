# KUBERNETES CHEATS

# General 

## Set up Prompt

```
echo 'source <(kubectl completion bash)' >> ~/.bashrc
```

# Kubernetes Cluster Commands 

### Display Cluster information
```kubectl cluster-info```

### List all nodes in the cluster and show IPs
``` kubectl get nodes -o wide ```

##  Kubernetes pod commands

### List all the pods
``` kubectl get pods ```

### Show detailed information about a pod
``` kubectl get pods -o wide ```

### Show all the pods that have a specific label 
``` kubectl get pods -l <label>=<value>```

### Show one specific pod 
``` kubectl get pods <name>```

### Show a pod's details
```kubect describe pod``` 

### View logs of a pod
```kubectl logs <pod>```

### Execute a command inside a pod
```kubectl exec -it <pod>```

### Delete a pod
``` kubectl delete pod <pod>```


### Displays an overview of the Pod resource
``` kubectl explain pod <resource>```


# Kubernetes Deployment Commands 