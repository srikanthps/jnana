# Chapter 9: CI/CD, Releases, and Developer Experience

Fast delivery requires automated validation, safe deployment, and simple developer workflows.

## CI Tools

Use GitHub Actions, GitLab CI, CircleCI, Buildkite, Jenkins, Azure Pipelines, Tekton, or Argo Workflows.

## CD Tools

Use Argo CD or Flux for GitOps-based continuous delivery.

## Deployment Strategies

Support:

- Rolling deployments
- Blue/green deployments
- Canary deployments
- Feature flags
- Tenant-by-tenant rollout
- Region-by-region rollout
- Cloud-by-cloud rollout

## Progressive Delivery

Use Argo Rollouts, Flagger, Istio, Linkerd, NGINX canary annotations, AWS App Mesh, or cloud-native traffic controls.

## Container Builds

Use Docker BuildKit, Kaniko, Buildah, Cloud Native Buildpacks, Bazel, Earthly, or Dagger.

Images should be pushed to ECR, Azure Container Registry, Google Artifact Registry, GitHub Container Registry, GitLab Container Registry, Harbor, or JFrog Artifactory.

## Developer Experience

Local and preview environments can use Docker Compose, Dev Containers, Tilt, Skaffold, Telepresence, Garden, Okteto, Minikube, Kind, k3d, or Rancher Desktop.

## Feature Management

Use LaunchDarkly, Unleash, Flagsmith, ConfigCat, Split, or OpenFeature.

Feature flags should support tenant-level targeting, kill switches, audit logs, and progressive rollout.
