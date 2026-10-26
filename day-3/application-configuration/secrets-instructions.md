Instructions
============

Create a new secret from the manifest:
```
my-secret.yaml
```

**List all secrets**
```
oc get secrets
```

**Describe the secret**
```
oc describe secret my-secret
```

**Let's create a Pod that uses this secret**
```
apiVersion: v1
kind: Pod
metadata:
    name: mysql-lockerd
spec:
  containers:
  - image: mysql:8-debian
    name: mysql
    env:
      - name: MYSQL_ROOT_PASSWORD
        valueFrom:
          secretKeyRef:
            name: my-secret
            key: password
```
