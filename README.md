# Udemy Course Microservices with Spring Boot, Docker, Kubernetes Section_16
https://www.udemy.com/course/master-microservices-with-spring-docker-kubernetes/
## spring version: 3.4.5
## gatewayservice version: 3.5.0
## Java 21
## Kubernetes: kind 1.23.5 


## Creating our own Helm chart

### in helm folder
helm create eazybank-common
Creating eazybank-common

### in eazybank-services folder
helm create accounts
Creating accounts

### in accounts folder
helm dependencies build
Hang tight while we grab the latest from your chart repositories...
...Successfully got an update from the "kubernetes-dashboard" chart repository
...Successfully got an update from the "bitnami" chart repository
Update Complete. ⎈Happy Helming!⎈
Saving 1 charts
Deleting outdated charts


## Helm chart for environments

### in environments folder
helm create dev-env
Creating dev-env

### in dev-env folder
helm dependencies build
Hang tight while we grab the latest from your chart repositories...
...Successfully got an update from the "kubernetes-dashboard" chart repository
...Successfully got an update from the "bitnami" chart repository
Update Complete. ⎈Happy Helming!⎈
Saving 8 charts
Deleting outdated charts


## Install KeyCloak

### in keycloak folder after download from Bitnami repository
helm dependencies build
Hang tight while we grab the latest from your chart repositories...
...Successfully got an update from the "kubernetes-dashboard" chart repository
...Successfully got an update from the "bitnami" chart repository
Update Complete. ⎈Happy Helming!⎈
Saving 2 charts
Downloading postgresql from repo oci://registry-1.docker.io/bitnamicharts
Pulled: registry-1.docker.io/bitnamicharts/postgresql:16.6.6
Digest: sha256:a8a0fd5ecbec861cc8462a417a8804c182caa2ee1666abc1a0f8a7f9126c2e40
Downloading common from repo oci://registry-1.docker.io/bitnamicharts
Pulled: registry-1.docker.io/bitnamicharts/common:2.31.0
Digest: sha256:972d8a92610885563a58618911368868481aab8fbf9f3daf083cf6d90994c1d9
Deleting outdated charts

### in helm folder
helm install keycloak keycloak
NAME: keycloak
LAST DEPLOYED: Tue Jul 22 22:13:09 2025
NAMESPACE: default
STATUS: deployed
REVISION: 1
TEST SUITE: None
NOTES:
CHART NAME: keycloak
CHART VERSION: 24.8.0
APP VERSION: 26.3.1
...


## Install KeyCloak

### in kafka folder after download from Bitnami repository
helm dependencies build
Hang tight while we grab the latest from your chart repositories...
...Successfully got an update from the "kubernetes-dashboard" chart repository
...Successfully got an update from the "bitnami" chart repository
Update Complete. ⎈Happy Helming!⎈
Saving 1 charts
Downloading common from repo oci://registry-1.docker.io/bitnamicharts
Pulled: registry-1.docker.io/bitnamicharts/common:2.31.0
Digest: sha256:972d8a92610885563a58618911368868481aab8fbf9f3daf083cf6d90994c1d9
Deleting outdated charts

### in helm folder
helm install kafka kafka
NAME: kafka
LAST DEPLOYED: Wed Jul 23 13:01:26 2025
NAMESPACE: default
STATUS: deployed
REVISION: 1
TEST SUITE: None
NOTES:
CHART NAME: kafka
CHART VERSION: 32.3.6
APP VERSION: 4.0.0
...


## Install Prometheus

### in kube-prometheus folder after download from Bitnami repository
helm dependencies build
Hang tight while we grab the latest from your chart repositories...
...Successfully got an update from the "kubernetes-dashboard" chart repository
...Successfully got an update from the "bitnami" chart repository
Update Complete. ⎈Happy Helming!⎈
Saving 4 charts
Downloading node-exporter from repo oci://registry-1.docker.io/bitnamicharts
Pulled: registry-1.docker.io/bitnamicharts/node-exporter:4.5.11
Digest: sha256:609e8010b1bce57a219d2b51271066e556256e52deac3c25abed1acf5c2e3d11
Downloading kube-state-metrics from repo oci://registry-1.docker.io/bitnamicharts
Pulled: registry-1.docker.io/bitnamicharts/kube-state-metrics:5.0.6
Digest: sha256:6362d05afe0cce25fc5dd667a1ba76305e0bebd2954895b32d9dda468b59d10e
Downloading common from repo oci://registry-1.docker.io/bitnamicharts
Pulled: registry-1.docker.io/bitnamicharts/common:2.31.0
Digest: sha256:972d8a92610885563a58618911368868481aab8fbf9f3daf083cf6d90994c1d9
Deleting outdated charts

### in helm folder
helm install prometheus kube-prometheus
NAME: prometheus
LAST DEPLOYED: Wed Jul 23 16:07:29 2025
NAMESPACE: default
STATUS: deployed
REVISION: 1
TEST SUITE: None
NOTES:
CHART NAME: kube-prometheus
CHART VERSION: 11.2.16
APP VERSION: 0.84.0
...


## Install Grafana Loki

### in grafana-loki folder after download from Bitnami repository
helm dependencies build
Hang tight while we grab the latest from your chart repositories...
...Successfully got an update from the "kubernetes-dashboard" chart repository
...Successfully got an update from the "bitnami" chart repository
Update Complete. ⎈Happy Helming!⎈
Saving 6 charts
Downloading grafana-alloy from repo oci://registry-1.docker.io/bitnamicharts
Pulled: registry-1.docker.io/bitnamicharts/grafana-alloy:1.0.0
Digest: sha256:ddb8e0b01af350a4eee64d7631d8252ab2f4617f6b26d87cc7724496cd552c1d
Downloading memcached from repo oci://registry-1.docker.io/bitnamicharts
Pulled: registry-1.docker.io/bitnamicharts/memcached:7.9.3
Digest: sha256:fb348332ff7e2cb414f0d79338cca37101d458c49c981a2a5b7385e45c622331
Downloading memcached from repo oci://registry-1.docker.io/bitnamicharts
Pulled: registry-1.docker.io/bitnamicharts/memcached:7.9.3
Digest: sha256:fb348332ff7e2cb414f0d79338cca37101d458c49c981a2a5b7385e45c622331
Downloading memcached from repo oci://registry-1.docker.io/bitnamicharts
Pulled: registry-1.docker.io/bitnamicharts/memcached:7.9.3
Digest: sha256:fb348332ff7e2cb414f0d79338cca37101d458c49c981a2a5b7385e45c622331
Downloading memcached from repo oci://registry-1.docker.io/bitnamicharts
Pulled: registry-1.docker.io/bitnamicharts/memcached:7.9.3
Digest: sha256:fb348332ff7e2cb414f0d79338cca37101d458c49c981a2a5b7385e45c622331
Downloading common from repo oci://registry-1.docker.io/bitnamicharts
Pulled: registry-1.docker.io/bitnamicharts/common:2.31.3
Digest: sha256:924aa307587ee64855387a9506103b59e1c1c0664b49d43b715ed5307281afbb
Deleting outdated charts

### in helm folder
helm install loki grafana-loki
NAME: loki
LAST DEPLOYED: Wed Jul 23 16:40:51 2025
NAMESPACE: default
STATUS: deployed
REVISION: 1
TEST SUITE: None
NOTES:
CHART NAME: grafana-loki
CHART VERSION: 6.0.0
APP VERSION: 3.5.2
...


## Install Grafana Tempo

### in grafana-tempo folder after download from Bitnami repository
helm dependencies build
Hang tight while we grab the latest from your chart repositories...
...Successfully got an update from the "kubernetes-dashboard" chart repository
...Successfully got an update from the "bitnami" chart repository
Update Complete. ⎈Happy Helming!⎈
Saving 2 charts
Downloading memcached from repo oci://registry-1.docker.io/bitnamicharts
Pulled: registry-1.docker.io/bitnamicharts/memcached:7.8.1
Digest: sha256:0ccbd4137b2a31f068e342c87ffcce7623aeea756c5ecb344215050b8a87941a
Downloading common from repo oci://registry-1.docker.io/bitnamicharts
Pulled: registry-1.docker.io/bitnamicharts/common:2.31.0
Digest: sha256:972d8a92610885563a58618911368868481aab8fbf9f3daf083cf6d90994c1d9
Deleting outdated charts

### in helm folder
helm install tempo grafana-tempo
NAME: tempo
LAST DEPLOYED: Wed Jul 23 16:57:35 2025
NAMESPACE: default
STATUS: deployed
REVISION: 1
TEST SUITE: None
NOTES:
CHART NAME: grafana-tempo
CHART VERSION: 4.0.13
APP VERSION: 2.8.1
...
