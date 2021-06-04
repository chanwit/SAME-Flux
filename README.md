# SAME / GitOps Retrained Flowers - Infra Repo

This is a Flux v2 configuration repo for the SAME / GitOps Retrained Flowers demo.

To get started:

Install Flux v2 CLI (tested with Flux v2 0.13.4)
```
brew install fluxcd/tap/flux
```

Then, obtain your GitHub token and set it to GITHUB_TOKEN environment variable.
```
export GITHUB_TOKEN=<your github token>
```

For the staging environment (Azure-based), to test bootstrap the KFP cluster, run `flux bootstrap` command like this.
```
flux bootstrap github \
  --owner=<your repo location> \
  --repository=SAME-Flux \
  --path=./cluster-stage \
  --token-auth \
  --network-policy=false
```

For the production environment, bootstrap with the following command.
```
flux bootstrap github \
  --owner=<your repo location> \
  --repository=SAME-Flux \
  --path=./cluster-prod \
  --token-auth \
  --network-policy=false
```

This configuration should be later a part of the SAME repo template.
