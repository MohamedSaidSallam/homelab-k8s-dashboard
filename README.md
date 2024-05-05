# HOMELAB-K8S-DASHBOARD

Wrapper for [kubernetes-dashboard helm chart](https://artifacthub.io/packages/helm/k8s-dashboard/kubernetes-dashboard)

## Run

```sh
helm upgrade --install --create-namespace -n kubernetes-dashboard kubernetes-dashboard . --wait --wait-for-jobs --timeout 3m
# OR --atomic
```

## Updating Dependencies

```sh
rm -rf charts && helm dep update && cd charts && for filename in *.tgz; do tar -xf "$filename" && rm -f "$filename"; done; cd ..
```
