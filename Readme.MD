# Note: We usually choose ebc with dynamic volume provision because volume and servers are placed at same location.

* How to create and delete all pods?
```
kubectl apply -f namespace.yaml
```
```
kubectl apply -f expense-ebs-dynamic-sc.yaml
```

```
kubectl apply -f mysql/manifest.yaml
```
```
kubectl apply -f backend/manifest.yaml
```
```
kubectl apply -f frontend/manifest.yaml
```
```
kubectl apply -f debug/manifest.yaml
```

```
kubectl delete pods --all -n your-namespace
```

# How to test or debug mysql data using Debug pod
```
kubectl exec -it debug -n expense -- /bin/bash
```
```
mysql -h mysql -u root -pExpenseApp@1
```