# Practical Questions on Pod Creation

### Question 1: Create a Pod with Image Nginx using Declarative Way
Create a YAML file named pod.yaml with the following content:

```
apiVersion: v1
kind: Pod
metadata:
  name: mypod
spec:
  containers:
    - name: my-first-container
      image: nginx
```

- Apply the YAML file using the command: 
```
kubectl apply -f pod.yaml
```
- Check the state of the Pod using: 
```
kubectl get po
```

### Question 2: Replace the Image of the Pod from Nginx to Busybox
To replace the image of the pod from Nginx to Busybox, modify the pod.yaml file, changing the image field to busybox. Then, apply the changes by running the same command used in Question 1:
```
kubectl apply -f pod.yaml
```

### Question 3: Check the Status of the Pod
To check the status of the pod, use the following command:
```
kubectl get pod
```

This command will display the current state and details of all pods in the cluster.

### Question 4: Delete the Pod
To delete the pod, use the following command:
```
kubectl delete pod mypod
```

This command will remove the specified pod named mypod from the cluster.
