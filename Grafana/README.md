Begin adding the repos to Helm for the installation. Run these commands: 

helm repo add prometheus-community https://prometheus-community.github.io/helm-charts
helm repo add grafana https://grafana.github.io/helm-charts

the command "helm repo list" should show "grafana" and "prometheus" among the list.

Install the prometheus helm chart:
helm install prometheus prometheus-community/kube-prometheus-stack

Install the grafana helm chart:
helm install loki grafana/loki-stack

helm list You should have a cluster like this in the default namespace with Prometheus, grafana and loki installed.
