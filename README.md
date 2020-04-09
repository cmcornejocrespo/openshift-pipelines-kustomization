# Kustomization for Deploying OpenShift Pipelines (Tekton)

This kustomization uses [tektoncd-pipeline-operator](https://github.com/openshift/tektoncd-pipeline-operator).

## Deploying OpenShift Pipelines

```
$ oc apply --kustomize openshift-pipelines-operator/base
```

```
$ oc apply --kustomize openshift-pipelines-instance/base
```
## Deploying a dashboard for Tekton

```
$ curl \
    --location \
    https://github.com/tektoncd/dashboard/releases/download/v0.6.1/openshift-tekton-dashboard-release.yaml \
    | sed --expression 's|namespace: tekton-pipelines|namespace: openshift-pipelines|g' \
    | oc apply --filename -
```
