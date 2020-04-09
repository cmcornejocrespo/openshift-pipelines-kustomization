# Kustomization for Deploying OpenShift Pipelines (Tekton)

This kustomization uses [tektoncd-pipeline-operator](https://github.com/openshift/tektoncd-pipeline-operator).

## Deploying OpenShift Pipelines

Install openshift-pipelines-operator using:
```
$ oc apply --kustomize openshift-pipelines-operator/base
```

Verify that the operator is running:

```
$ oc get pod --namespace openshift-operators | grep pipelines
openshift-pipelines-operator-9cdbbb854-rhzsx   1/1     Running   0          98s
```

Deploy openshift-pipelines control plane:

```
$ oc apply --kustomize openshift-pipelines-instance/base
```

Verify that the openshift-pipelines control plane pods are running:

```
$ oc get pod --namespace openshift-pipelines
NAME                                         READY   STATUS    RESTARTS   AGE
tekton-pipelines-controller-cbbbb9b6-tgxtc   1/1     Running   0          28s
tekton-pipelines-webhook-5d467b4747-hlfxx    1/1     Running   0          28s
```

## Using OpenShift Pipelines

Download the Tekton CLI (*tkn*) by following the [installation instructions](https://github.com/tektoncd/cli#installing-tkn).

Refer to the [OpenShift Pipelines Tutorial](https://github.com/openshift/pipelines-tutorial).
