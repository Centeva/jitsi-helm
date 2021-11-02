# Centeva Jitsi

Fork of a Jitsi helm chart used to install Jitsi in a cluster.

## Table of Contents

1. [About the Project](#about-the-project)
    * [Built With](#built-with)
2. [Installation](#installation)
6. [Contributing](#contributing)

## About The Project

### Built With

* [Jitsi](https://jitsi.org/)
* [Chart-releaser-action](https://github.com/helm/chart-releaser-action)
* [jisi-helm (forked chart)](https://github.com/krakazyabra/jitsi-helm)

## Installation

### Using helm

```sh
helm repo add centeva-jitsi https://centeva.github.io/jitsi-helm
helm install jitsi centeva-jitsi/centeva-jitsi
```

### Using Kustomize

*kustomization.yml*
```yml
apiVersion: kustomize.config.k8s.io/v1beta1
kind: Kustomization
namespace: jitsi
helmCharts:
  - name: jitsi
    repo: https://centeva.github.io/jitsi-helm
    releaseName: centeva-jitsi
```
## Contributing

Pushing to main will automatically deploy a new version of the chart using the release.yml workflow.