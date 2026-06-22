# Exercise 21: Production ALB Ingress Setup

## Objective

Expose three applications through AWS Application Load Balancer.

## Routes

- `/api/*` routes to `api-service`
- `/admin/*` routes to `admin-service`
- `/dashboard/*` routes to `dashboard-service`

## Requirements Covered

- SSL using ACM certificate annotation
- HTTP to HTTPS redirection on port 443
- Target group health checks using `/health`

## Apply

```powershell
kubectl apply -f .\alb-ingress.yaml
```

## Validation

```powershell
kubectl get ingress production-apps-alb
kubectl describe ingress production-apps-alb
```
