# DeployMultipleApplicationsUsingOnlyAHelmChart

This Helm chart deploy multiple applications using the apps node declared in the file values.yaml


values.yaml

....

apps: \
  app1: \
    name: "app1" \
    containerPort: 80 \
    livenessProbePath: / \
    readinessProbePath: / \
    image: \
      repository: nginx \
      pullPolicy: IfNotPresent \
      tag: "" \
  app2: \
    name: "app2" \
    containerPort: 80 \
    livenessProbePath: / \
    readinessProbePath: / \
    image: \
      repository: prydonius/todo \
      pullPolicy: IfNotPresent \
      tag: 1.0.0 \



# Usage

Execute these commands:

helm install all all/
kubectl get all

Enjoy :)
