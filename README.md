# connect-to-kubernetes-cluster-from-localterminal
You can connect to your cluster via command-line or using a dashboard.
Configure kubectl command line access by running the following command:
```
gcloud container clusters get-credentials standard-cluster-1 --zone us-central1-a --project elegant-expanse-90876
kubectl get nodes
