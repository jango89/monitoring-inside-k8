# monitoring

Used to boot up Grafana, Alertmanager and Prometheus for Kubernetes Cluster monitoring.

**How it works**

Kube-state-metrics, node-exporter and mysql-exporter exports metrics from all kubernetes resources and mysql cluster.
Prometheus is used to store this metrics which is then used as a datasource for Grafana.
Alerts/dashboards to monitor JVM services, kubernetes cluster resources and mysql resource is available.

**Nice to have**

1. Right now any alerts, dashboards or other configuration changes needs restarting of respective services. 
   Example: for change in alerts(prometheus needs to be restarted) and for change in dashboards(grafana needs to be restarted).
