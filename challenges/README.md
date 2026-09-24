# Kubernetes / OpenShift Troubleshooting Lab

This lab contains 10 deliberately broken manifests for troubleshooting practice.

## Learner setup

Create a namespace/project:

    kubectl create namespace troubleshooting

or OpenShift:

    oc new-project troubleshooting

Apply one exercise at a time:

    kubectl apply -f 01-imagepull.yaml -n troubleshooting

or:

    oc apply -f 01-imagepull.yaml -n troubleshooting

Then investigate without looking at the instructor answers.

## Useful commands

    oc get pods
    oc get all
    oc get events --sort-by=.lastTimestamp
    oc describe pod <pod>
    oc logs <pod>
    oc get svc
    oc get endpoints
    oc get pvc
    oc get storageclass

For minikube, use kubectl instead of oc.

## Exercises

    01 ImagePullBackOff
    02 CrashLoopBackOff
    03 Service selector mismatch
    04 Wrong Service targetPort
    05 Missing ConfigMap
    06 Missing Secret
    07 Readiness probe failure
    08 PVC Pending
    09 RBAC / Forbidden
    10 Unschedulable due to resource requests
