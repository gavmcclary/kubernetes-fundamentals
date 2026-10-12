
Useful Commands
===============

**Logs**

We can view container logs with the following command:

```
oc logs <pod-name>
```
**First check you have minikube running**
```
minikube start
```

Apply the manifest: **counter.yaml**

What is the problem with using the command **oc logs counter**?
```
oc logs counter
```

**View specific container logs:**

```
oc logs counter -c countby3
```

**View all containers:**

```
oc logs counter --all-containers
```
