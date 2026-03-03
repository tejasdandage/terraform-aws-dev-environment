# Terraform AWS Dev Environment

This project provisions AWS infrastructure using Terraform.

## Resources Created

- Custom VPC
- Public Subnet
- Internet Gateway
- Route Table + Association
- Security Group (SSH + HTTP)
- EC2 (t3.micro - Free Tier eligible)
- SSH Key managed by Terraform

## Commands Used

terraform init  
terraform plan  
terraform apply  
terraform destroy  

## Errors Faced & Fixes

- terraform: command not found → Installed via Homebrew
- Duplicate provider configuration → Removed duplicate provider block
- InvalidKeyPair.NotFound → Created key using aws_key_pair resource
- Instance type not free tier → Changed t2.micro → t3.micro

## Cleanup

Use:
terraform destroy

to avoid unwanted AWS charges.