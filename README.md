# Installing-Prometheus

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

###
