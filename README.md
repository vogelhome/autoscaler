# Fork
[![REUSE status](https://api.reuse.software/badge/github.com/gardener/autoscaler)](https://api.reuse.software/info/github.com/gardener/autoscaler)

This is a fork of [kubernetes/autoscaler](https://github.com/kubernetes/autoscaler) developed for the [gardener/machine-controller-manager](https://github.com/gardener/machine-controller-manager) and [gardener/gardener](https://github.com/gardener/gardener) project.   

Find more details about this fork in [FORK.md](./FORK.md).

**TL;DR** Support for Machine-controller-manager is added to cluster-autoscaler. It means cluster-autoscaler now works for all cloud-providers which MCM supports which are AWS, GCP, Azure, Openstack, Alibaba, Packet, vSphere.

# Kubernetes Autoscaler

[![Release Charts](https://github.com/kubernetes/autoscaler/actions/workflows/release.yaml/badge.svg)](https://github.com/kubernetes/autoscaler/actions/workflows/release.yaml) [![Tests](https://github.com/kubernetes/autoscaler/actions/workflows/ci.yaml/badge.svg)](https://github.com/kubernetes/autoscaler/actions/workflows/ci.yaml) [![GoDoc Widget]][GoDoc]

This repository contains autoscaling-related components for Kubernetes.

## What's inside

[Cluster Autoscaler](https://github.com/kubernetes/autoscaler/tree/master/cluster-autoscaler) - a component that automatically adjusts the size of a Kubernetes
Cluster so that all pods have a place to run and there are no unneeded nodes. Supports several public cloud providers. Version 1.0 (GA) was released with kubernetes 1.8.

[Vertical Pod Autoscaler](https://github.com/kubernetes/autoscaler/tree/master/vertical-pod-autoscaler) - a set of components that automatically adjust the
amount of CPU and memory requested by pods running in the Kubernetes Cluster. Current state - beta.

[Addon Resizer](https://github.com/kubernetes/autoscaler/tree/master/addon-resizer) - a simplified version of vertical pod autoscaler that modifies
resource requests of a deployment based on the number of nodes in the Kubernetes Cluster. Current state - beta.

[Charts](https://github.com/kubernetes/autoscaler/tree/master/charts) - Supported Helm charts for components above.

## Contact Info

Interested in autoscaling? Want to talk? Have questions, concerns or great ideas?

Please join us on #sig-autoscaling at https://kubernetes.slack.com/, or join one
of our weekly meetings.  See [the Kubernetes Community Repo](https://github.com/kubernetes/community/blob/master/sig-autoscaling/README.md) for more information.

## Getting the Code

Fork the repository in the cloud:
1. Visit https://github.com/kubernetes/autoscaler
1. Click Fork button (top right) to establish a cloud-based fork.

The code must be checked out as a subdirectory of `k8s.io`, and not `github.com`.

```shell
mkdir -p $GOPATH/src/k8s.io
cd $GOPATH/src/k8s.io
# Replace "$YOUR_GITHUB_USERNAME" below with your github username
git clone https://github.com/$YOUR_GITHUB_USERNAME/autoscaler.git
cd autoscaler
```

Please refer to Kubernetes [Github workflow guide] for more details.

[GoDoc]: https://godoc.org/k8s.io/autoscaler
[GoDoc Widget]: https://godoc.org/k8s.io/autoscaler?status.svg
[Github workflow guide]: https://github.com/kubernetes/community/blob/master/contributors/guide/github-workflow.md
