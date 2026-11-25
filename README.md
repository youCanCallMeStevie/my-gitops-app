# my-gitops-app

A tiny nginx web page used to learn GitOps with Argo CD, then orchestrate the same app with Harness.

```
app/        Kubernetes manifests Argo CD deploys (configmap, deployment, service)
argocd/     The Argo CD Application definition (kept outside app/ on purpose)
```

## Try the GitOps loop
1. Edit `replicas` in `app/deployment.yaml` or the "Version" text in `app/configmap.yaml`.
2. `git commit` and `git push`.
3. Refresh in Argo CD, see the app go OutOfSync, then Sync.
