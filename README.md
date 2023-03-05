# Function as service in Kubernetes

## K8S for lab test

```bash
kind create cluster --name knative --config ~/project/kubernetes/kind/config.yml
```

## Test result

```bash
kubectl -n kourier-system port-forward services/kourier 3000:80
```

```bash
curl -H "Host: helloworld-go.default.example.com" http://localhost:3000
```