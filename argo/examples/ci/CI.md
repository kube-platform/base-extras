# CI using Argo Events

[Argo Events](https://github.com/argoproj/argo-events) is an addition to Argo Workflows.

This example constists of 3 components

- A Github Gateway, that adds a Github Webhook using a Githubn personal access token
- A Webhook Gateway, that receives push/commit/... events from Github
- A Github Sensor, that creates a workflow when an event is received

## Adoptions to own CI

- Change the token of __github-access.properties__ to the ones of your account and choose a Webhook secret
- Setup repository information in __go-example-build.properties__
- Change the Webhook Ingress resource to what you have defined in __go-example-build.properties__
- Change the workflow to be triggered in github/sensor.yaml