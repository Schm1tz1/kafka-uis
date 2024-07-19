# Coduktor UI
* Docs: https://www.conduktor.io/
* Source: https://github.com/conduktor/conduktor-platform
* Helc Charts: https://helm.conduktor.io/

## Installation
* Spin up PostgreSQL database (mandatory):
```shell
kubectl apply -f psqgl.yaml
```

* Installation of a base Conduktor Console:
```shell
helm repo add conduktor https://helm.conduktor.io
helm repo update

helm install console conduktor/console \
  --create-namespace -n conduktor \
  --values values.yaml 
```

* Forward port (or create ingress):
```shell
kubectl port-forward -n conduktor svc/console 8080:80
```
