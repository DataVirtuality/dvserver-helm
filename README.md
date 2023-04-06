# DV Platform chart

This repository contains the official DV Platform Helm chart for installing and configuring DV Platform on Kubernetes.
The chart deploys a StatefulSet with a single pod consisted of two mandatory and one optional container:
the DV Platform main mandatory container, a PostgreSQL v13 sidecar container -- this is also mandatory container
as DV Platform requires a PostgreSQL configuration database for normal work -- and optional Filebeat container
that allows to collect all DV Platform logs an upload them to an external logs collection database.


## Prerequisites

To use the charts here, [Helm](https://helm.sh/) version 3 must be configured for your
Kubernetes cluster. Setting up Kubernetes and Helm is outside the scope of
this README. Please refer to the Kubernetes and Helm documentation.


## Usage

To install the latest version of this chart, add the DV Platform helm repository
and run `helm install`:

```console
$ helm repo add dvplatform https://datavirtuality.github.io/dvserver-helm/
"dvplatform" has been added to your repositories

$ helm install dvplatform dvplatform/dvplatform
```

Please see the many options supported in the `values.yaml` file.