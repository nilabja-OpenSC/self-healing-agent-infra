# self-healing-agent-infra

### Follow the steps to Deploy

### clone the repository with the branches

git clone

### switch to branch deploy-test

git checkout deploy-test

### Check the code with helm command

helm template observability ./self-healing-agent-infra --namespace nilabja-haldar-dev --set global.platform=openshift --set global.expose.type=route

### Deploy the infra

helm install observability ./self-healing-agent-infra --namespace nilabja-haldar-dev --set global.platform=openshift --set global.expose.type=route
