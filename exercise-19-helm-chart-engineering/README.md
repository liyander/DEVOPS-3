# Exercise 19: Helm Chart Engineering

## Objective

Build a reusable Helm chart with environment-specific values.

## Structure

```text
reusable-app-chart/
  Chart.yaml
  values.yaml
  values-dev.yaml
  values-qa.yaml
  values-prod.yaml
  templates/
```

## Supported Features

- Replicas
- Resources
- ConfigMaps
- Secrets
- Ingress
- Autoscaling
- Environment values for dev, qa, and prod

## Commands

```powershell
helm lint .\reusable-app-chart
helm template dev .\reusable-app-chart -f .\reusable-app-chart\values-dev.yaml
helm template qa .\reusable-app-chart -f .\reusable-app-chart\values-qa.yaml
helm template prod .\reusable-app-chart -f .\reusable-app-chart\values-prod.yaml
helm install reusable-app .\reusable-app-chart -f .\reusable-app-chart\values-dev.yaml
```
