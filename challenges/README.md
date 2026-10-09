# Kubernetes / OpenShift Troubleshooting Lab

This lab contains 10 deliberately broken manifests for troubleshooting practice.

## Learner setup

Create a namespace/project:

    oc create namespace troubleshooting

or OpenShift:

    oc new-project troubleshooting

Apply one exercise at a time:

    oc apply -f 01.yaml -n troubleshooting

or:

    oc apply -f 01.yaml -n troubleshooting

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

    01 ?
    02 ?
    03 ?
    04 ?
    05 ?
    06 ?
    07 ?
    08 ?
