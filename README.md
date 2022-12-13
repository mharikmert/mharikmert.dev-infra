# mharikmert.dev-infra
Continuous delivery for [mharikmert.dev](https://mharikmert.dev)'s infrastructure using FluxCD and GitOps on Kubernetes

## Flux Bootstrap command with extra-components
```bash
flux bootstrap github \
  --components-extra=image-reflector-controller,image-automation-controller \
  --owner=$GITHUB_USER \
  --repository=mharikmert.dev-infra \
  --branch=master \
  --path=clusters/mharikmert.dev \
  --read-write-key \
  --personal
  ```


## Architecture
![infra drawio](https://user-images.githubusercontent.com/42295478/207407608-9fe26ea4-3ffa-4c86-bf99-319ccb477827.svg)
