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
![infra drawio](https://user-images.githubusercontent.com/42295478/213651979-c0df1cdc-4a58-4697-9c6b-ac36693a0d56.svg)

