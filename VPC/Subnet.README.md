# Step 3: Create a Private Subnet

## Objective

The objective of this task was to create a private subnet within my Virtual Private Cloud (VPC). A private subnet is used to host resources that should not be directly accessible from the internet, such as databases, application servers, and internal services.

## Steps Performed

1. Logged in to the AWS Management Console.
2. Searched for **VPC** and opened the **VPC Dashboard**.
3. Selected **Subnets** from the left navigation pane.
4. Clicked **Create subnet**.
5. Selected the VPC I had previously created.
6. Entered the following details:
   - **Subnet name:** Private-Subnet
   - **Availability Zone:** Selected an Availability Zone (e.g., eu-west-2b)
   - **IPv4 CIDR block:** `10.0.2.0/24`
7. Clicked **Create subnet**.

## Result

The private subnet was successfully created inside my VPC. This subnet is designed to host resources that do not require direct internet access, providing an additional layer of security.

## What I Learned

- A private subnet does not have a route to an Internet Gateway.
- Resources in a private subnet cannot be accessed directly from the internet.
- Private subnets are commonly used for databases, backend applications, and internal services.
- Separating resources into public and private subnets improves network security and follows AWS best practices.

## Skills Demonstrated

- Amazon VPC
- Private Subnet Configuration
- AWS Networking
- CIDR Block Planning
- Cloud Infrastructure
- AWS Management Console
