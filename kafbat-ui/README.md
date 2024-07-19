# OpenSource kafbat UI
* Docs: https://ui.docs.kafbat.io/
* Source: https://github.com/kafbat/kafka-ui

## Installation
Quick installation with values for a default plaintext CP cluster in `confluent` namespace:
```shell
helm repo add kafbat-ui https://kafbat.github.io/helm-charts
helm install kafbat-ui kafbat-ui/kafka-ui --create-namespace -n kafbat --values values.yaml
```

* Forward port (or create ingress):
```shell
kubectl port-forward -n kafbat svc/kafbat-ui-kafka-ui 8080:80
```