# Kustomization for Deploying OpenShift Pipelines (Tekton)

This kustomization uses [tektoncd-pipeline-operator](https://github.com/openshift/tektoncd-pipeline-operator).

```
$ oc apply --kustomize openshift-pipelines-operator/base
```

```
$ oc apply --kustomize openshift-pipelines-instance/base
```
