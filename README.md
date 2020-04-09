# Kustomization for Deploying OpenShift Pipelines (Tekton)

This kustomization uses [tektoncd-pipeline-operator](https://github.com/openshift/tektoncd-pipeline-operator).

## Deploying OpenShift Pipelines

```
$ oc apply --kustomize openshift-pipelines-operator/base
```

```
$ oc apply --kustomize openshift-pipelines-instance/base
```

## Using OpenShift Pipelines

Download the Tekton CLI (*tkn*) by following the [download instructions](https://github.com/tektoncd/cli#installing-tkn).

Refer to the [OpenShift Pipelines Tutorial](https://github.com/openshift/pipelines-tutorial).
