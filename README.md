# learn-terraform-azure
Getting started with Terraform on Azure

## Prerequisites
- [Azure CLI](https://docs.microsoft.com/en-us/cli/azure/install-azure-cli?view=azure-cli-latest)
- [Terraform](https://www.terraform.io/downloads.html)

## Steps
1. Login to Azure CLI
```
az login
```
2. Create a Service Principal for Terraform
```
az ad sp create-for-rbac --role="Contributor" --scopes="/subscriptions/<subscription_id>"
```
3. Create a `terraform.tfvars` file and add the following variables
```
subscription_id = "<subscription_id>"
client_id = "<client_id>"
client_secret = "<client_secret>"
tenant_id = "<tenant_id>"
```
4. Initialize Terraform
```
terraform init
```
5. Create a Terraform plan
```
terraform plan -out plan
```
6. Apply the Terraform plan
```
terraform apply plan
```
7. Destroy the Terraform plan
```
terraform destroy
```
    
