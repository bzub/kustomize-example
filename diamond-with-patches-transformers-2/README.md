Example shared transformers for https://kubernetes.slack.com/archives/C9A5ALABG/p1573757274293200

## `kustomize build base`
```yaml
apiVersion: v1
kind: Service
metadata:
  name: my-service
spec:
  ports:
  - name: http
    port: 80
---
apiVersion: extensions/v1beta1
kind: Deployment
metadata:
  name: my-deployment
spec:
  template:
    spec:
      containers:
      - image: my-image
        name: my-deployment
```

## `kustomize build overlays/dev`
```yaml
apiVersion: v1
kind: Service
metadata:
  name: my-service
  namespace: company-dev
spec:
  ports:
  - name: http
    port: 80
---
apiVersion: extensions/v1beta1
kind: Deployment
metadata:
  name: my-deployment
  namespace: company-dev
spec:
  template:
    spec:
      containers:
      - image: my-image
        name: my-deployment
```
