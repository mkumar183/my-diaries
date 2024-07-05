https://www.youtube.com/watch?v=VOruC2tQbmw

What is Lens ? 
  IDE for K8S. 

What is Helm Chart ?
  Its a bundle of configurations that allow you to deploy a set of resources, services and configurations. Think of it as a package of cloudformation templates. 
  Common helm charts are available in helm repositories. like python or java packages / libraries. 


Notes from Udemy Training: 
https://powerschool.udemy.com/course/amazon-eks-starter-kubernetes-on-aws/learn/lecture/31872772#overview

Concepts: 
What does AWS does for EKS Management ? 
Amazon EKS Cluster: Master Nodes, etcd and worker nodes. 

Node Groups: Under node groups you can scale number of nodes. Which means within a nodegroup you might be running similar services. So like to understand UIHN Architecture of how we utilize K8S cluster for scaling our applications there. 


Step 1: Basic Setup 
- Takes care of Master nodees and etcd. Only worker nodes are to be managed by us. 
- Already have aws cli installed on my machine 
- aws configure sso is what we will use 
- az client is already installed
- copied eksctl from https://eckctl.io downloaded .exe 
- copied .exe to C:\windows\system32 something thats there in %PATH% variable
- from command prompt can run `eksctl version` and getting 0.165.0 
- kubectl is already installed : `kubectl version --client  `

Step 2: Create a EKS Cluster using eksctl: 
- look at website https://eksctl.io for commands it provides 
- run `eksctl create cluster`

here is the list of things i got: 
There are 2 roles available to you.
 error UnauthorizedOperation: You are not authorized to perform this operation. User: arn:aws:iam::443260147495:user/mk_internal_data is not authorized to perform: ec2:DescribeAvailabilityZones because no identity-based policy allows the ec2:DescribeAvailabilityZones action
PS C:\Users\kumarman\insight-git-repos\diary-technical-execution\AWS-EKS-Udemy-master-revised\c-EKS-Setup\c.a-eksctl> eksctl create cluster -f .\eks-course.yaml
2023-12-09 22:17:42 [ℹ]  eksctl version 0.165.0
2023-12-09 22:17:42 [ℹ]  using region us-west-2
2023-12-09 22:17:44 [ℹ]  skipping us-west-2d from selection because it doesn't support the following instance type(s): t2.small
2023-12-09 22:17:44 [ℹ]  setting availability zones to [us-west-2b us-west-2c us-west-2a]
2023-12-09 22:17:44 [ℹ]  subnets for us-west-2b - public:192.168.0.0/19 private:192.168.96.0/19
2023-12-09 22:17:44 [ℹ]  subnets for us-west-2c - public:192.168.32.0/19 private:192.168.128.0/19
2023-12-09 22:17:44 [ℹ]  subnets for us-west-2a - public:192.168.64.0/19 private:192.168.160.0/19
2023-12-09 22:17:45 [ℹ]  nodegroup "ng-1" will use "ami-019e5b81636e5a350" [AmazonLinux2/1.27]
Error: cannot find EC2 key pair "eks-course"
PS C:\Users\kumarman\insight-git-repos\diary-technical-execution\AWS-EKS-Udemy-master-revised\c-EKS-Setup\c.a-eksctl> eksctl create cluster -f .\eks-course.yaml
2023-12-09 22:19:22 [ℹ]  eksctl version 0.165.0
2023-12-09 22:19:22 [ℹ]  using region us-west-2
2023-12-09 22:19:23 [ℹ]  skipping us-west-2d from selection because it doesn't support the following instance type(s): t2.small
2023-12-09 22:19:23 [ℹ]  setting availability zones to [us-west-2a us-west-2c us-west-2b]        
2023-12-09 22:19:23 [ℹ]  subnets for us-west-2a - public:192.168.0.0/19 private:192.168.96.0/19  
2023-12-09 22:19:23 [ℹ]  subnets for us-west-2c - public:192.168.32.0/19 private:192.168.128.0/19
2023-12-09 22:19:23 [ℹ]  subnets for us-west-2b - public:192.168.64.0/19 private:192.168.160.0/19
2023-12-09 22:19:25 [ℹ]  nodegroup "ng-1" will use "ami-019e5b81636e5a350" [AmazonLinux2/1.27]
2023-12-09 22:19:25 [ℹ]  using Kubernetes version 1.27
2023-12-09 22:19:25 [ℹ]  creating EKS cluster "EKS-course-cluster" in "us-west-2" region with un-managed nodes
2023-12-09 22:19:25 [ℹ]  1 nodegroup (ng-1) was included (based on the include/exclude rules)
2023-12-09 22:19:25 [ℹ]  will create a CloudFormation stack for cluster itself and 1 nodegroup stack(s)
2023-12-09 22:19:25 [ℹ]  will create a CloudFormation stack for cluster itself and 0 managed nodegroup stack(s)
2023-12-09 22:19:25 [ℹ]  if you encounter any issues, check CloudFormation console or try 'eksctl utils describe-stacks --region=us-west-2 --cluster=EKS-course-cluster'
2023-12-09 22:19:25 [ℹ]  Kubernetes API endpoint access will use default of {publicAccess=true, privateAccess=false} for cluster "EKS-course-cluster" in "us-west-2"
2023-12-09 22:19:25 [ℹ]  CloudWatch logging will not be enabled for cluster "EKS-course-cluster" in "us-west-2"
2023-12-09 22:19:25 [ℹ]  you can enable it with 'eksctl utils update-cluster-logging --enable-types={SPECIFY-YOUR-LOG-TYPES-HERE (e.g. all)} --region=us-west-2 --cluster=EKS-course-cluster'
2023-12-09 22:19:25 [ℹ]
2 sequential tasks: { create cluster control plane "EKS-course-cluster",
2023-12-09 22:25:40 [ℹ]  waiting for CloudFormation stack "eksctl-EKS-course-cluster-cluster"
2023-12-09 22:26:41 [ℹ]  waiting for CloudFormation stack "eksctl-EKS-course-cluster-cluster"
2023-12-09 22:28:44 [ℹ]  waiting for CloudFormation stack "eksctl-EKS-course-cluster-cluster"
2023-12-09 22:30:54 [ℹ]  building nodegroup stack "eksctl-EKS-course-cluster-nodegroup-ng-1"
2023-12-09 22:30:54 [ℹ]  --nodes-min=3 was set automatically for nodegroup ng-1
2023-12-09 22:30:54 [ℹ]  --nodes-max=3 was set automatically for nodegroup ng-1
2023-12-09 22:30:57 [ℹ]  deploying stack "eksctl-EKS-course-cluster-nodegroup-ng-1"
2023-12-09 22:30:57 [ℹ]  waiting for CloudFormation stack "eksctl-EKS-course-cluster-nodegroup-ng-1"
2023-12-09 22:31:28 [ℹ]  waiting for CloudFormation stack "eksctl-EKS-course-cluster-nodegroup-ng-1"
2023-12-09 22:32:19 [ℹ]  waiting for CloudFormation stack "eksctl-EKS-course-cluster-nodegroup-ng-1"
2023-12-09 22:33:01 [ℹ]  waiting for CloudFormation stack "eksctl-EKS-course-cluster-nodegroup-ng-1"
2023-12-09 22:34:09 [ℹ]  waiting for CloudFormation stack "eksctl-EKS-course-cluster-nodegroup-ng-1"
2023-12-09 22:35:01 [ℹ]  waiting for CloudFormation stack "eksctl-EKS-course-cluster-nodegroup-ng-1"
2023-12-09 22:36:58 [ℹ]  waiting for CloudFormation stack "eksctl-EKS-course-cluster-nodegroup-ng-1"
2023-12-09 22:36:59 [ℹ]  waiting for the control plane to become ready
2023-12-09 22:37:00 [✔]  saved kubeconfig as "C:\\Users\\kumarman\\.kube\\config"
2023-12-09 22:37:00 [ℹ]  no tasks
2023-12-09 22:37:00 [✔]  all EKS cluster resources for "EKS-course-cluster" have been created
2023-12-09 22:37:02 [ℹ]  adding identity "arn:aws:iam::443260147495:role/eksctl-EKS-course-cluster-nodegrou-NodeInstanceRole-8o7JSEAKN8Lf" to auth ConfigMap
2023-12-09 22:37:03 [ℹ]  nodegroup "ng-1" has 0 node(s)
2023-12-09 22:37:03 [ℹ]  waiting for at least 3 node(s) to become ready in "ng-1"
2023-12-09 22:38:09 [ℹ]  nodegroup "ng-1" has 3 node(s)
2023-12-09 22:38:09 [ℹ]  node "ip-192-168-23-58.us-west-2.compute.internal" is ready
2023-12-09 22:38:09 [ℹ]  node "ip-192-168-51-131.us-west-2.compute.internal" is ready
2023-12-09 22:38:09 [ℹ]  node "ip-192-168-75-223.us-west-2.compute.internal" is ready
2023-12-09 22:38:12 [ℹ]  kubectl command should work with "C:\\Users\\kumarman\\.kube\\config", try 'kubectl get nodes'
2023-12-09 22:38:12 [✔]  EKS cluster "EKS-course-cluster" in "us-west-2" region is ready
PS C:\Users\kumarman\insight-git-repos\diary-technical-execution\AWS-EKS-Udemy-master-revised\c-EKS-Setup\c.a-eksctl> kubectl get nodes
NAME                                           STATUS   ROLES    AGE     VERSION
ip-192-168-23-58.us-west-2.compute.internal    Ready    <none>   4m47s   v1.27.7-eks-e71965b
ip-192-168-51-131.us-west-2.compute.internal   Ready    <none>   4m45s   v1.27.7-eks-e71965b
ip-192-168-75-223.us-west-2.compute.internal   Ready    <none>   4m44s   v1.27.7-eks-e71965b
PS C:\Users\kumarman\insight-git-repos\diary-technical-execution\AWS-EKS-Udemy-master-revised\c-EKS-Setup\c.a-eksctl>

- to overcome the error to mk_internal_data i allowed adminaccess
- now when i go to aws i do not see the cluster and stack 
- to see the cluster and the stack in the aws i have to change the region to us-west-2 

Checkpoint: Resources created by eksctl create cluster : 
- EC2 instances for Master node 
- Security Groups 
- Auto Scaling Groups (for master node across availability zones)

