# Shared configmap example

A configmap in the base has its REGION key merged from different
configurations.

Try:
```sh
# namespace1 region1
kustomize build namespace1/region1

# namespace1 region2
kustomize build namespace1/region2

# namespace2 region1
kustomize build namespace2/region1

# namespace2 region2
kustomize build namespace2/region2
```
