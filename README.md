# Terraform Development Environment on AWS

This project provisions a development environment on AWS using Terraform. It demonstrates how to automate the setup of cloud infrastructure, including VPCs, subnets, security groups, and an EC2 instance with Docker pre-installed.

## Project Structure

- `providers.tf`: Configures the AWS provider for Terraform.
- `main.tf`: Defines the core infrastructure, including VPC, subnet, internet gateway, security groups, and EC2 instance.
- `userdata.tpl`: Shell script to install Docker on the EC2 instance during startup.
- `datasources.tf`: Retrieves the latest Ubuntu AMI from AWS.

## Requirements

- AWS Account
- Terraform v1.5+
- AWS CLI configured with credentials

## Setup

1. Clone this repository:
   ```bash
   git clone https://github.com/Mzokhulayo/terraform-development-environment.git

2. Initialize terraform:
   - terraform init
3. Review and apply the Terraform plan:
   - terraform plan
   - terraform apply
4. SSH into the EC2 instance after deployment:
   - sh -i path_to_your_key.pem ubuntu@your_ec2_public_ip
   - once inside the development run _docker --version_ to check the version of docker installed withyour instance creation
