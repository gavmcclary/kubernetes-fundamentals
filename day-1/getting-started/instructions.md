Instructions
=============

Create namespace: **troubleshooting**

```
oc project troubleshooting
```
Apply the manifest **basic-pod.yaml**

```
oc apply -f basic-pod.yaml -n troubleshooting
```

Check pod is running:

```
oc get pods
```


***CHALLENGE: Why isn't the Pod showing as Running?***

**Useful commands**

```
oc get pod basic-pod
oc describe pod basic-pod
oc logs basic-pod
```
