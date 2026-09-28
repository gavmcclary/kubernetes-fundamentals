**Pre-requisites**

It is assumed learner has the *oc* command line installed already

*Podman*

```
brew install podman
```
```
podman machine init
```

```
podman machine start
```

**Minikube**

```
brew install minikube 
```

```
minikube start --driver=podman
```

```
minikube config set driver podman
```

Test Minikube is running:

```
username@XXXXXXXXX ~ % oc project 

Using project "default" from context named "minikube" on server "https://127.0.0.1:39987".

username@XXXXXXXXX ~ % oc get ns

NAME              STATUS   AGE
default           Active   50s
kube-node-lease   Active   50s
kube-public       Active   50s
kube-system       Active   50s
```
