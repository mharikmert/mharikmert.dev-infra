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

![infra](https://user-images.githubusercontent.com/42295478/204051062-d51bccc5-2428-4a57-8b6a-35ef559e52ad.svg)

<!-- TODO: Add flux-system components and image update automation -->
