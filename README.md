terraform-eks
A sample repository to create EKS on AWS using Terraform.

Install AWS CLI
As the first step, you need to install AWS CLI as we will use the AWS CLI (aws configure) command to connect Terraform with AWS in the next steps.

**Follow the below link to Install AWS CLI**.

https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html
Install Terraform
Next, Install Terraform using the below link.

https://developer.hashicorp.com/terraform/tutorials/aws-get-started/install-cli
Connect Terraform with AWS
Its very easy to connect Terraform with AWS. Run aws configure command and provide the AWS Security credentials as shown in the video.

**Initialize Terraform**
Clone the repository and Run terraform init. This will intialize the terraform environment for you and download the modules, providers and other configuration required.

Optionally review the terraform configuration

**Run terraform plan to see the configuration it creates when executed.**
![Screenshot (682)](https://github.com/saurabhjoshi8624/TerraformForEks/assets/119957235/53d10a58-8d8b-4967-bed6-ae2f74d7af83)


Finally, Apply terraform configuation to create EKS cluster with VPC
terraform apply

Finally our cluster is deployed on AWS.

2. **Now We have to deploy sample snake game application on k8s**
   
we have deployment file as well as Service file to expose our application,

**hello.yml**

![Screenshot dep](https://github.com/saurabhjoshi8624/TerraformForEks/assets/119957235/ea54741f-ad40-43e3-92ae-b36f1687b8f6)

**3.Then we have command to apply using**
'''
kubectl apply -f hello.yml

'''
After appying this file Deployment as well as Service will create and we expose it on Port no 30001 of NodePort service.


let's check createted dep and svc

![Screenshot files](https://github.com/saurabhjoshi8624/TerraformForEks/assets/119957235/cb87e19a-25e4-4905-9ae4-44b181666835)


now copy the any node public ip and give the port no. 

in our case 54.83.157.122:30001

![Screenshot (692)](https://github.com/saurabhjoshi8624/TerraformForEks/assets/119957235/78c6ba73-fec0-41d7-89cc-d456fb7a8a5b)



**And open in it on browser. so we have successfully deployed sample game application** 


![Screenshot app](https://github.com/saurabhjoshi8624/TerraformForEks/assets/119957235/5c3d9537-ecdd-4d42-8eea-bab7cda0efdc)





