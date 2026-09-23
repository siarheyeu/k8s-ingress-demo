
# k8s-ingress-demo

A minimal Kubernetes demo showing how to expose an application using Ingress.

## Files

- deployment.yaml — Deployment with probes and resource limits
- service.yaml — ClusterIP service for internal routing
- ingress.yaml — Ingress rule exposing the app via host `demo.local`

## Apply

kubectl apply -f deployment.yaml
kubectl apply -f service.yaml
kubectl apply -f ingress.yaml

## Check

kubectl get pods
kubectl get svc
kubectl get ingress

## Test

Add to /etc/hosts:

127.0.0.1 demo.local

Then open:

http://demo.local
