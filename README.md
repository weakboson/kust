# kust

## Overlay weakboson

```shell
kustomize build overlays/weakboson
```

```yml
apiVersion: v1
kind: Deployment
metadata:
  labels:
    app.kubernetes.io/managed-by: kustomize
    app.kubernetes.io/name: sample
    developer: weakboson
  name: weakboson-sample
spec:
  selector:
    matchLabels:
      app.kubernetes.io/name: sample
      developer: weakboson
  template:
    metadata:
      labels:
        app.kubernetes.io/name: sample
        developer: weakboson
    spec:
      containers:
      - image: rails:weakboson-xxxxx
        name: app
```

## Overlay gluon

```shell
kustomize build overlays/gluon
```

```yml
apiVersion: v1
kind: Deployment
metadata:
  labels:
    app.kubernetes.io/managed-by: kustomize
    app.kubernetes.io/name: sample
    developer: gluon
  name: gluon-sample
spec:
  selector:
    matchLabels:
      app.kubernetes.io/name: sample
      developer: gluon
  template:
    metadata:
      labels:
        app.kubernetes.io/name: sample
        developer: gluon
    spec:
      containers:
      - image: rails:gluon-yyyyy
        name: app
```