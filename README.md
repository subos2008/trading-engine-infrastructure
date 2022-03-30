# trading-engine-infrastructure

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
