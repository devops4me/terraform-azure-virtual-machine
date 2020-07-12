
# Use Terraform to Create an Azure Virtual Machine

We are going to provision a virtual machine within the Microsoft Azure cloud using Terraform. We can use either Linux, Mac or Windows to run the terraform plan and apply.

## Pre-Conditions

Before you provision the machine ensure that you have
- **terraform** installed
- an **Azure** account
- the **Azure CLI** installed on the machine running terraform


## Steps to Install the Azure Virtual Machine with Terraform

Log into Azure using the Azure CLI.

```
az login
```

In the browser that pops up select your Azure account and log in. The JSON resulting from the login will state the **subscription ID**, the **tenant ID**, the **home tenant ID** and the **user name**.

Now in the terminal issue these commands.

```
git clone https://github.com/devops4me/terraform-azure-virtual-machine
terraform init
terraform plan
terraform apply -auto-approve
#  Now check that the resource group and VM infrastructure were created
terraform destroy -auto-approve
```

