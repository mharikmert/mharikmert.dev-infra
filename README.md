# mharikmert.dev-infra
Continuous delivery workflow for [mharikmert.dev](https://mharikmert.dev)'s infrastructure using FluxCD and GitOps on Kubernetes

## Flux Bootstrap command with extra-components
```bash
flux bootstrap github \
  --components-extra=image-reflector-controller,image-automation-controller \
  --owner=$GITHUB_USER \
  --repository=mharikmert.dev-infra \
  --branch=master \
  --path=clusters/mharikmert.dev \
  --read-write-key \
  --version=v2.0.0 # set the toolkit version to avoid upgrading the latest version in each bootstrap. 
  ```
## Architecture
You can view the architecture from https://infra.mharikmert.dev
