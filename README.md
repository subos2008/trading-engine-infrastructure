# trading-engine-infrastructure

# IN PROCESS OF DEPRICATION

This repo is for the k8 version of the trading engine deployment.  It adds Redis and Datadog's agent to a Kubernetes cluster using Flux.

However, I'm in the process of porting it (day 1) to ecs/serverless AWS
See: https://github.com/subos2008/trading-engine-infrastructure-v2-aws

See:
1. https://fluxcd.io/docs/get-started/
2. https://fluxcd.io/docs/guides/repository-structure/
  * https://github.com/fluxcd/flux2-kustomize-helm-example

# Cheatsheet
* flux uninstall
* flux bootstrap github \\n  --owner=subos2008 \\n  --repository=trading-engine-infrastructure \\n  --branch=main \\n  --path=./clusters/production \\n  --personal
* flux logs --kind Kustomization --all-namespaces
* flux get all
* flux check
* watch flux get helmreleases --all-namespaces
* flux reconcile kustomization infrastructure --with-source
