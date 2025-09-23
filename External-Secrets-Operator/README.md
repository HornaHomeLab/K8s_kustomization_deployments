# External Secrets Operator Setup


1. Install required CRDs
```shell
helm install external-secrets external-secrets/external-secrets --namespace external-secrets-operator --create-namespace
```

2. Create a `secret.yaml` in appropriate overlays sub directory with the following format:

```YAML
apiVersion: v1
kind: Secret
metadata:
  name: vault-approle-secret
type: Opaque
data:
  secret-id: <replace-with-approle-secret-id>
```
