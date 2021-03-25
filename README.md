# SAME-Flux

This is a Flux v2 configuration template repo to help you preparing a SAME cluster.

To get started:

Install Flux v2 CLI (tested with Flux v2 0.10.0)
```
brew install fluxcd/tap/flux
```

Then, obtain your GitHub token and set it to GITHUB_TOKEN environment variable.
```
export GITHUB_TOKEN=<your github token>
```

To test bootstrap the KFP cluster, run `flux bootstrap` command like this.
```
flux bootstrap github \
  --owner=SAME-Project \
  --repository=SAME-Flux \
  --token-auth --path=cluster
```

This configuration should be later a part of the SAME repo template.
