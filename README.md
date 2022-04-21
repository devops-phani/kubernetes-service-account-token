# kubernetes-service-account-token

### Get Kubernetes service account token

```
kubectl get secret $(kubectl get serviceaccount developer -o jsonpath="{.secrets[0].name}") -o jsonpath="{.data.token}" | base64 --decode
```
