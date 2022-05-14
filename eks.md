# Security Best Practices

**least privileged access**

Do not use [*] inside rolebinding and clusterrolebinding and make sure to provide exact granular level necessary access insitead of giving full access.

**make the EKS cluster endpoint private**

By default eks cluster endpoint is public. Even if EKS cluster endpoint is public, any API request comes must be authenticated via IAM and authorized by Kubernetes RBAC. 

[1] Cluster Endpoint can be private.
[2] Cluster endpoint can be public and specify which CIDR blocks can communicate with cluster endpoint. 
[3] Cluster endpoint access can be mixed of private and public access. Public access can be restricted through specific whitelisted CIDR block while any communiation between kubelet (worker nodes) and control plane is via cross account elastic network interfaces (which git provisioned when control plane getting provisioned). 

**create the cluster with dedicated IAM role**
Create eks cluster with dedicated IAM role. This access cannot be removed and is not managed through the aws-auth ConfigMap. Regularly audit to view who can assume this role. 

## AWS Load Balancer Controller

Prerequisites - 

1. running eks cluster
2. AWS CLI is available.
3. eksctl is installed to work.



