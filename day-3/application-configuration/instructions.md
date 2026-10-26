Instructions
============

**Download the file:
```
treats.txt**
```

**Create ConfigMap from the treats.txt file**
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

**Once Pod has started, exec into it**
```
oc exec -it nginx -- sh
```

***Check contents of Pod**
```
ls
```

**You should see the *treats* directory listed**
```
bin  boot  dev	etc  home  lib	media  mnt  opt  proc  root  run  sbin	srv  sys  tmp  treats  usr  var
```

**Move into the *treats* directory**
```
cd treats
```

**And view the contents of file *treats.txt***
```
cat treats.txt
```
```
Cookie
Muffin
Brownie
Blondie
```

**Challenge: What happens if you delete the Pod and re apply the manifest?**
