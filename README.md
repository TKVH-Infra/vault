# vault
Kubernetes deployment with all secrets hidden in an Hashicorp Vault.

## Requirements after unseal for vault csi

```
vault write auth/k8s-vault-csi/config \
  kubernetes_host=https://10.43.0.1:443 \
  bound_service_account_names=vault-k8s-auth \
  disable_iss_validation=true
```
