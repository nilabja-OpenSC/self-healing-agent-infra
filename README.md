# self-healing-agent-infra

### Follow the steps to Deploy

### clone the repository with the branches

git clone https://github.com/nilabja-OpenSC/self-healing-agent-infra.git

### switch to branch deploy-test

git checkout deploy-test

### Change the namespace name in values.yaml file

global:<br>
&nbsp;&nbsp;&nbsp;namespace: `<your namespace name>`

### Check the code with helm command

helm template observability ./self-healing-agent-infra --namespace `<your namespace name>` --set global.platform=openshift --set global.expose.type=route

### Deploy the infra

helm install observability ./self-healing-agent-infra --namespace `<your namespace name>` --set global.platform=openshift --set global.expose.type=route

Note: There is an issue with Postgressql Db. Ignore it as of now.
