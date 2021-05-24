# GitHub Action for Tekton

This GitHub Action configures [`tkn`](https://github.com/tektoncd/cli) in the environment for managing [Tekton](https://tekton.dev/) 
resources in GitHub Actions. 

Tekton is a powerful yet flexible Kubernetes-native open-source framework for creating continuous integration and 
delivery (CI/CD) systems. It lets users build, test, and deploy across multiple cloud providers or on-premises systems 
by abstracting away the underlying implementation details.

## Prerequisites

Connect to your Kubernetes Cluster or configure it using Kubernetes in Docker

```yaml
- uses: engineerd/setup-kind@v0.5.0
```

Install Tekton Pipelines 

```yaml
- run: kubectl apply --filename https://storage.googleapis.com/tekton-releases/pipeline/latest/release.yaml
```

## Usage

`jerop/tkn` installs `tkn` for your operating system 

```yaml
- uses: jerop/tkn@v0.1.0
```

## Version

`jerop/tkn` installs the latest version of `tkn` by default - use `version` to select a specific version of `tkn`

```yaml
- uses: jerop/tkn@v0.1.0
  with:
    version: v0.18.0
```

## Demo

Use of Tekton and GitHub Actions is demonstrated in https://github.com/jerop/demo-tkn

