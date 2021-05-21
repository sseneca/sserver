# sseneca's k8s server

This repository contains the deploy files for my server.

## Architecture

This is for a bare-metal cluster. Currently it contains one node that
runs [Parabola GNU/Linux-libre](https://www.parabola.nu/).

Kubernetes is ran via [k3s](https://k3s.io). [Flux](https://fluxcd.io/)
is used for GitOps as well as automating e.g. image upgrades. I try to
use Helm charts whenever I can via the [Helm
Controller](https://fluxcd.io/docs/components/helm/) Secrets are
[sealed](https://github.com/bitnami-labs/sealed-secrets).

## Caveats

Node configuration isn't included, but is very simple:

- Install an OS
- Install k3s (one-liner)
- Bootstrap Flux (~one-liner)
