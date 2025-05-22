# AWS VPC Architecture Project

## Overview

This project demonstrates the setup of a Virtual Private Cloud (VPC) in AWS, incorporating both public and private subnets, an Internet Gateway, and a NAT Gateway to facilitate secure and efficient network communication.

## Architecture Diagram

![Architecture Diagram](https://github.com/user-attachments/assets/616b468e-f4a3-4f3f-bbe7-79b0655eb5ab))

## Components

- **VPC CIDR**: `10.0.0.0/16`
- **Public Subnet**: `10.0.1.0/24` – Hosts resources that need direct internet access.
- **Private Subnet**: `10.0.2.0/24` – Contains resources without direct internet exposure.
- **Internet Gateway (IGW)**: Enables internet access for resources in the public subnet.
- **NAT Gateway**: Allows instances in the private subnet to initiate outbound traffic to the internet.
- **Route Tables**: Configured to direct traffic appropriately between subnets and gateways.
- **Security Groups**: Define inbound and outbound traffic rules for instances.

## Deployment Steps

1. **Create VPC** with the specified CIDR block.
2. **Set up Subnets**: One public and one private.
3. **Attach Internet Gateway** to the VPC.
4. **Configure Route Tables** for both subnets.
5. **Launch EC2 Instances** in respective subnets.
6. **Set up NAT Gateway** in the public subnet.
7. **Test Connectivity** to ensure proper configuration.

## Testing

1. Try accessing public ec2 instance in browser using public IP---gets success as you allowed traffic on port 80
2. Try accessing private ec2 instance in browser using public IP---fails as you only allowed traffic from public ec2 instance.

## Learnings

Through this project, I gained insights into:

- Designing a multi-tier network architecture in AWS.
- Configuring secure access between public and private resources.
- Implementing best practices for network segmentation and traffic control.

## References

- [AWS VPC Documentation](https://docs.aws.amazon.com/vpc/latest/userguide/what-is-amazon-vpc.html)
- [AWS Subnetting](https://docs.aws.amazon.com/vpc/latest/userguide/VPC_Subnets.html)
