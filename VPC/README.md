# Step 1: Create a Virtual Private Cloud (VPC)

## Objective

The objective of this task was to create a Virtual Private Cloud (VPC), which provides a private and secure network where AWS resources such as EC2 instances can be deployed.

## Steps Performed

1. Logged in to the AWS Management Console.
2. Searched for **VPC** in the AWS search bar and opened the **VPC Dashboard**.
3. Clicked **Create VPC**.
4. Selected **VPC only** as the resource to create.
5. Entered the following details:
   - **Name tag:** My-VPC
   - **IPv4 CIDR block:** `10.0.0.0/16`
   - **IPv6 CIDR block:** None
   - **Tenancy:** Default
6. Reviewed the configuration.
7. Clicked **Create VPC**.

## Result

The VPC was successfully created and became available in the VPC Dashboard. This VPC serves as the foundation for building a secure AWS network and will host additional networking components such as subnets, route tables, and an Internet Gateway.

## What I Learned

- A VPC is a logically isolated virtual network in AWS.
- Every AWS resource must be launched inside a VPC.
- The CIDR block defines the range of IP addresses available within the VPC.
- A VPC provides complete control over networking, including IP addressing, routing, and security.

## Skills Demonstrated

- Amazon VPC
- AWS Networking
- CIDR Block Configuration
- AWS Management Console
- Cloud Infrastructure
