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
