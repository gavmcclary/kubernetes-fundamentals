Instructions
============

**Create ConfigMap from txt file**
```
oc create configmap treats --from-file=treats.txt
```

**View all ConfigMaps**
```
oc get configmaps
```

**View a specific ConfigMap**
```
oc describe configmap <configmap-name>
```

**Create the following Pod**
```
apiVersion: v1
kind: Pod
metadata:
  name: nginx
spec:
  containers:
    - name: nginx
      image: nginx:1.14.2
      # Step 2:
      volumeMounts:
        - name: sweet-treats
          mountPath: /treats
# STEP 1: Add the ConfigMap as a volume to this pod
  volumes:
    - name: sweet-treats
      configMap:
        name: treats

```

**And apply the manifest**
```
oc apply -f <pod-manifest-yaml-file>
```

