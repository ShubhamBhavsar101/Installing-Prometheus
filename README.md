# Installing Prometheus and Grafana
Installing-Prometheus and Grafana using Helm Charts


### Install helm
```bash
sudo snap install helm --classic
```

### Install Prometheus
```bash
helm repo add prometheus-community https://prometheus-community.github.io/helm-charts
helm repo update
helm install prometheus prometheus-community/prometheus
```

### Expose Nodeport for access
```bash
k expose service prometheus-server --type=NodePort --target-port=9090 --name=prometheus-server-ext
k get svc
minikube ip
```

- Access using [minikube ip]:[NodePort]


# Installing Grafana

```bash
helm repo add grafana https://grafana.github.io/helm-charts
helm repo update
helm install grafana grafana/grafana
```

### Expose Nodeport for access
```bash
k expose service grafana --type=NodePort --target-port=3000 --name=grafana-ext
k get svc
minikube ip
```

- Access using [minikube ip]:[NodePort]
