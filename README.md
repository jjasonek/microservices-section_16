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
