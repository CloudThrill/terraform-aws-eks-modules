# Terraform AWS EKS Modules

Reusable Terraform modules for AWS EKS infrastructure components.

## Modules

- **aws-networking/aws-vpc** - Custom VPC with EKS-optimized subnets
- **aws-eks** - EKS cluster with managed node groups
- **eks-blueprints-addons** - Common EKS add-ons (ALB, EBS, monitoring)
- **eks-data-addons** - Data and ML-specific EKS add-ons

## Usage

### VPC
```hcl
module "vpc" {
  source = "git::https://github.com/cloudthrill/terraform-aws-eks-modules.git//aws-networking/aws-vpc?ref=v1.0.0"
  # ... configuration
}
```

### EKS
```hcl
module "eks" {
  source = "git::https://github.com/cloudthrill/terraform-aws-eks-modules.git//aws-eks?ref=v1.0.0"
  # ... configuration
}
```

### Core Add-ons
```hcl
module "eks_addons" {
  source = "git::https://github.com/cloudthrill/terraform-aws-eks-modules.git//eks-blueprints-addons?ref=v1.0.0"
  # ... configuration
}
```

### Data Add-ons (AI and Big Data)
```hcl
module "data_addons" {
  source = "git::https://github.com/cloudthrill/terraform-aws-eks-modules.git//eks-data-addons?ref=v1.0.0"
  # ... configuration
}
```
