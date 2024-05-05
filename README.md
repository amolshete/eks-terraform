### Follow Below Instructions to create the AWS EKS infra with Terraform 

Prerequisite: Terraform tool setup with aws credential configuration, kubectl tool, aws cli tool

Steps:
 1.  Clone the code using below command

 ```
 git clone https://github.com/amolshete/eks-terraform.git
 ```
 2. After cloning just check the values of the variables. If you want to make any changes you can do. Eg. In above repo we have considered the vpc region as "ap-south-1". Instead you can choose as per your choice. Just make other necessary changes as per that.
 
 3. You are ready to use terraform commands.
 ```
 terraform init
 terraform plan
 terraform apply 

 ```
 
 4.  To access your eks clutster, geneate the kubeconfig with below command
 ```
 aws eks update-kubeconfig --name <cluster-name> --region <region>

 ```
 Please note in above command you need to replace cluster name and region.
 Eg:
 ```
 aws eks update-kubeconfig --name my-cluster --region ap-south-1

 ```

5. And here we go. You can start using the kubectl commands.
```
kubectl get pods
```

6. Once your practise is done, if you wish to delete the eks cluster the simply use below command

```
terraform destroy
```
