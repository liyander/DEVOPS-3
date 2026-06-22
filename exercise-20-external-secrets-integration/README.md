# Exercise 20: External Secrets Integration

## Objective

Integrate AWS Secrets Manager with Kubernetes using External Secrets Operator.

## AWS Secrets Manager Value

Create a secret named `prod/app` with this JSON value:

```json
{
  "DB_USERNAME": "app_user",
  "DB_PASSWORD": "strong_password",
  "JWT_SECRET": "strong_jwt_secret"
}
```

## Apply

```powershell
kubectl apply -f .\service-account.yaml
kubectl apply -f .\secret-store.yaml
kubectl apply -f .\external-secret.yaml
```

## Validation

```powershell
kubectl get externalsecret
kubectl get secret app-secret
kubectl describe externalsecret app-external-secret
```
