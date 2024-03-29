
# What is Open Service Broker for Azure?

Open Service Broker for Azure is the open source, [Open Service Broker](https://www.openservicebrokerapi.org/)-compatible API server that provisions managed services in the Microsoft Azure public cloud.

# Prerequisites

In order to use the charts in this repository, you must have the following components installed:

1. A compatible [Kubernetes](https://github.com/kubernetes/kubernetes) cluster (version 1.7 or later)
1. [Helm](https://github.com/kubernetes/helm)
1. [Kubernetes Service Catalog](https://github.com/kubernetes-incubator/service-catalog)
1. [Open Service Broker for Azure](https://github.com/azure/open-service-broker-azure)

# Why use Bitnami Images?

* Bitnami closely tracks upstream source changes and promptly publishes new versions of this image using our automated systems.
* With Bitnami images the latest bug fixes and features are available as soon as possible.
* Bitnami containers, virtual machines and cloud images use the same components and configuration approach - making it easy to switch between formats based on your project needs.
* All our images are based on [minideb](https://github.com/bitnami/minideb) a minimalist Debian based container image which gives you a small base container image and the familiarity of a leading linux distribution.
* All Bitnami images available in Docker Hub are signed with [Docker Content Trust (DTC)](https://docs.docker.com/engine/security/trust/content_trust/). You can use `DOCKER_CONTENT_TRUST=1` to verify the integrity of the images.
* Bitnami container images are released daily with the latest distribution packages available.


> This [CVE scan report](https://quay.io/repository/bitnami/open-service-broker-azure?tab=tags) contains a security report with all open CVEs. To get the list of actionable security issues, find the "latest" tag, click the vulnerability report link under the corresponding "Security scan" field and then select the "Only show fixable" filter on the next page.

# Why use a non-root container?

Non-root container images add an extra layer of security and are generally recommended for production environments. However, because they run as a non-root user, privileged tasks are typically off-limits. Learn more about non-root containers [in our docs](https://docs.bitnami.com/containers/how-to/work-with-non-root-containers/).

# How to deploy Open Service Broker for Azure in Kubernetes?

You can find an example for testing in the file `test.yaml`. To launch this sample file run:

```bash
$ kubectl apply -f test.yaml
```

> NOTE: You have to edit test.yaml and set the parameters for SUBSCRIPTION_ID, TENANT_ID, CLIENT_ID, CLIENT_SCRECRET.

> NOTE: If you are pulling from a private containers registry, replace the image name with the full URL to the docker image. E.g.
>
> - image: 'your-registry/image-name:your-version'

# Supported tags and respective `Dockerfile` links

> NOTE: Debian 8 images have been deprecated in favor of Debian 9 images. Bitnami will not longer publish new Docker images based on Debian 8.

Learn more about the Bitnami tagging policy and the difference between rolling tags and immutable tags [in our documentation page](https://docs.bitnami.com/containers/how-to/understand-rolling-tags-containers/).


* [`1-debian-9`, `1.8.4-debian-9-r0`, `1`, `1.8.4`, `1.8.4-r0`, `latest` (1/debian-9/Dockerfile)](https://github.com/bitnami/bitnami-docker-open-service-broker-azure/blob/1.8.4-debian-9-r0/1/debian-9/Dockerfile)

Subscribe to project updates by watching the [bitnami/open-service-broker-azure GitHub repo](https://github.com/bitnami/bitnami-docker-open-service-broker-azure).

# Get this image

The recommended way to get the Bitnami Open Service Broker Azure Docker Image is to pull the prebuilt image from the [Docker Hub Registry](https://hub.docker.com/r/bitnami/open-service-broker-azure).

```bash
$ docker pull bitnami/open-service-broker-azure:latest
```

To use a specific version, you can pull a versioned tag. You can view the [list of available versions](https://hub.docker.com/r/bitnami/open-service-broker-azure/tags/) in the Docker Hub Registry.

```bash
$ docker pull bitnami/open-service-broker-azure:[TAG]
```

If you wish, you can also build the image yourself.

```bash
$ docker build -t bitnami/open-service-broker-azure:latest 'https://github.com/bitnami/bitnami-docker-open-service-broker-azure.git#master:1/debian-9'
```

# Configuration

# Further documentation

For further documentation, please check [here](https://github.com/Azure/open-service-broker-azure/tree/master/docs)

# Contributing

We'd love for you to contribute to this container. You can request new features by creating an [issue](https://github.com/bitnami/bitnami-docker-open-service-broker-azure/issues), or submit a [pull request](https://github.com/bitnami/bitnami-docker-open-service-broker-azure/pulls) with your contribution.

# Issues

If you encountered a problem running this container, you can file an [issue](https://github.com/bitnami/bitnami-docker-open-service-broker-azure/issues). For us to provide better support, be sure to include the following information in your issue:

- Host OS and version
- Docker version (`docker version`)
- Output of `docker info`
- Version of this container
- The command you used to run the container, and any relevant output you saw (masking any sensitive information)

# License

Copyright (c) 2019 Bitnami

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
