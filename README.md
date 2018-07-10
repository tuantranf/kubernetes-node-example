# kubernetes-node-example

## Local kubernetes environment
Kubectl
Minikube
Docker

## Start Minikube
```
$ minikube start
```

## Kubernetes Deployments & Services
```
# deployment
$ kubectl apply -f k8s

# confirm services
$ kubectl get services
NAME           TYPE           CLUSTER-IP      EXTERNAL-IP   PORT(S)          AGE
kubernetes     ClusterIP      10.96.0.1       <none>        443/TCP          6h
node-example   LoadBalancer   10.109.126.46   <pending>     3000:30001/TCP   6h

# confirm pods
$ kubectl get pods
NAME                                      READY     STATUS    RESTARTS   AGE
node-example-deployment-8fc69b486-wdf9v   1/1       Running   0          8m

# confirm deployment
$ kubectl get deployments
NAME                      DESIRED   CURRENT   UP-TO-DATE   AVAILABLE   AGE
node-example-deployment   1         1         1            1           8m

# access node-example service
$ minikube service node-example

# open dashboard
$ minikube dashboard

```
