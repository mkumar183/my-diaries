# use eksctl to create EKS cluster

display available options and properties:

```bash
eksctl create cluster --help
```

## creation

create cluster by using yaml config file:

```bash
eksctl create cluster -f eks-course.yaml
```

## post-install check

eksctl also creates the config file for _kubectl_. This means we can immediately fire up a check like:

```
kubectl get nodes
```
The above command works because there is a .kube/config file created which points it to the aws environment. C:\Users\kumarman\.kube\config

eksctl get cluster 
eksctl get nodegroups --cluster <clustername from prev cmd>

Each nodegroup is set of EC2s that is behind a loadbalancer ? 
scale nodegroup 
```
eksctl scale nodegroup --cluster EKS-course-cluster --nodes 5 --nodes-max 5 --name ng-1
```

```
eksctl get nodegroup --cluster EKS-course-cluster --region us-west-2 --name ng-1
```

```
kubectl get nodes
```
will also show you 5 nodes now. 
