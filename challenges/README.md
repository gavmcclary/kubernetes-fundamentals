# Kubernetes / OpenShift Troubleshooting Lab

This lab contains 8 deliberately broken manifests for troubleshooting practice.

## Learner setup

Create a namespace/project:

    oc create namespace troubleshooting

or OpenShift:

    oc new-project troubleshooting

Apply one exercise at a time:

    oc apply -f 01.yaml -n troubleshooting


Then investigate!

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


## Exercises

    01 ?
    02 ?
    03 ?
    04 ?
    05 ?
    06 ?
    07 ?
    08 ?
