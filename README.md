# Terraform AWS VPC Module

This Terraform module creates an AWS VPC with public and private subnets, an internet gateway, NAT gateway, and associated route tables.

## Usage

```hcl
module "vpc" {
  source = "github.com/<YOUR_USERNAME>/terraform-aws-vpc"

  vpc_cidr_block    = "10.0.0.0/16"
  private_subnet    = ["10.0.1.0/24", "10.0.2.0/24", "10.0.3.0/24"]
  public_subnet     = ["10.0.4.0/24", "10.0.5.0/24", "10.0.6.0/24"]
  availability_zone = ["ap-southeast-1a", "ap-southeast-1b", "ap-southeast-1c"]
}
