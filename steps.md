# Securing Kubernetes Ingress with Let's Encrypt

## 1. Use let's encrypt as CA

```bash
kubectl create ns vetify
kubectl apply -f vetify-certificate.yaml
kubectl -n vetify get secrets
```

## 2. Deploy pods and services

```bash
kubectl apply -f echo-deploy.yaml
kubectl apply -f proxy-deploy.yaml
```

## 3. Create ingress to handle http trafic

```bash
kubectl apply -f vetify-ingress.yaml
```
