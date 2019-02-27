# Federated Prometheus

```bash
oc create secret generic federated-scrape-configs --from-file=federated.yaml
oc create --filename prometheus.yaml
oc adm policy add-cluster-role-to-user prometheus-operator -z prometheus-operator --as=system:admin
```
