# Step 2: Create a Private Subnet

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

# Step 3: Create a Public Subnet

## Objective

The objective of this task was to create a public subnet within my Virtual Private Cloud (VPC). A public subnet is used to host resources that need direct access to the internet, such as web servers, load balancers, and bastion hosts.

## Steps Performed

1. Logged in to the AWS Management Console.
2. Searched for **VPC** and opened the **VPC Dashboard**.
3. Selected **Subnets** from the left navigation pane.
4. Clicked **Create subnet**.
5. Selected the VPC I had previously created.
6. Entered the following details:
   - **Subnet name:** Public-Subnet
   - **Availability Zone:** Selected an Availability Zone (for example, eu-west-2a)
   - **IPv4 CIDR block:** `10.0.1.0/24`
7. Clicked **Create subnet**.
8. After the subnet was created, selected the subnet.
9. Chose **Actions** → **Edit subnet settings**.
10. Enabled **Auto-assign public IPv4 address**.
11. Saved the changes.

## Result

The public subnet was successfully created and configured to automatically assign public IPv4 addresses to resources launched within it. This allows resources, when properly configured with an Internet Gateway and Route Table, to communicate with the internet.

## What I Learned

- A public subnet is a subnet that can provide internet access to its resources.
- Enabling **Auto-assign public IPv4 address** allows EC2 instances launched in the subnet to automatically receive a public IP address.
- A public subnet must be associated with a Route Table that routes internet traffic through an Internet Gateway.
- Public subnets are commonly used for web servers, application servers, and other internet-facing resources.

## Skills Demonstrated

- Amazon VPC
- Public Subnet Configuration
- IPv4 Address Management
- AWS Networking
- AWS Management Console
- Cloud Infrastructure


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

# Step 4: Create an Internet Gateway (IGW)

## Objective

The objective of this task was to create an Internet Gateway (IGW), which enables communication between resources in my Virtual Private Cloud (VPC) and the internet.

## Steps Performed

1. Logged in to the AWS Management Console.
2. Searched for **VPC** and opened the **VPC Dashboard**.
3. Selected **Internet Gateways** from the left navigation pane.
4. Clicked **Create internet gateway**.
5. Entered the following details:
   - **Name tag:** My-Internet-Gateway
6. Clicked **Create internet gateway**.

## Result

The Internet Gateway was successfully created and was ready to be attached to my VPC.

## What I Learned

- An Internet Gateway (IGW) is a VPC component that allows communication between a VPC and the internet.
- Creating an Internet Gateway alone does not provide internet access; it must be attached to a VPC.
- An Internet Gateway is required for resources in a public subnet to access the internet.

## Skills Demonstrated

- Amazon VPC
- Internet Gateway (IGW)
- AWS Networking
- Cloud Infrastructure
- AWS Management Console# Step 5: Attach the Internet Gateway to the VPC

## Objective

The objective of this task was to attach the Internet Gateway (IGW) to my Virtual Private Cloud (VPC). Attaching the Internet Gateway allows resources within the VPC to communicate with the internet when combined with the appropriate routing configuration.

## Steps Performed

1. Logged in to the AWS Management Console.
2. Searched for **VPC** and opened the **VPC Dashboard**.
3. Selected **Internet Gateways** from the left navigation pane.
4. Chose the Internet Gateway I had previously created.
5. Clicked **Actions**.
6. Selected **Attach to VPC**.
7. Chose my VPC from the list of available VPCs.
8. Clicked **Attach internet gateway**.

## Result

The Internet Gateway was successfully attached to my VPC. This completed a key networking configuration, allowing the VPC to communicate with the internet once the Route Table was updated with the appropriate route.

## What I Learned

- An Internet Gateway must be attached to a VPC before it can provide internet connectivity.
- Attaching an Internet Gateway alone does not give resources internet access.
- A Route Table must also include a default route (`0.0.0.0/0`) that points to the Internet Gateway.
- Resources in a public subnet can access the internet only after the Internet Gateway is attached and the Route Table is properly configured.

## Skills Demonstrated

- Amazon VPC
- Internet Gateway (IGW)
- VPC Configuration
- AWS Networking
- Cloud Infrastructure
- AWS Management Console# Step 7: Add a Route to the Internet Gateway

## Objective

The objective of this task was to configure the Route Table by adding a default route that directs internet-bound traffic to the Internet Gateway (IGW). This allows resources in the public subnet to communicate with the internet.

## Steps Performed

1. Logged in to the AWS Management Console.
2. Searched for **VPC** and opened the **VPC Dashboard**.
3. Selected **Route Tables** from the left navigation pane.
4. Chose the Route Table I had previously created.
5. Opened the **Routes** tab.
6. Clicked **Edit routes**.
7. Clicked **Add route**.
8. Entered the following values:
   - **Destination:** `0.0.0.0/0`
   - **Target:** Selected the Internet Gateway (IGW) attached to my VPC.
9. Clicked **Save changes**.

## Result

The Route Table was successfully updated with a default route that directs all internet-bound traffic to the Internet Gateway. This configuration enables resources in the associated public subnet to access the internet.

## What I Learned

- A route defines where network traffic should be directed.
- The destination `0.0.0.0/0` represents all IPv4 internet traffic.
- An Internet Gateway must be attached to the VPC before it can be selected as the target for a route.
- A public subnet requires a Route Table with a default route pointing to an Internet Gateway to enable internet connectivity.

## Skills Demonstrated

- Amazon VPC
- Route Table Configuration
- Internet Gateway (IGW)
- VPC Routing
- AWS Networking
- Cloud Infrastructure
- AWS Management Console

# Step 5: Attach the Internet Gateway to the VPC

## Objective

The objective of this task was to attach the Internet Gateway (IGW) to my Virtual Private Cloud (VPC). Attaching the Internet Gateway allows resources within the VPC to communicate with the internet when combined with the appropriate routing configuration.

## Steps Performed

1. Logged in to the AWS Management Console.
2. Searched for **VPC** and opened the **VPC Dashboard**.
3. Selected **Internet Gateways** from the left navigation pane.
4. Chose the Internet Gateway I had previously created.
5. Clicked **Actions**.
6. Selected **Attach to VPC**.
7. Chose my VPC from the list of available VPCs.
8. Clicked **Attach internet gateway**.

## Result

The Internet Gateway was successfully attached to my VPC. This completed a key networking configuration, allowing the VPC to communicate with the internet once the Route Table was updated with the appropriate route.

## What I Learned

- An Internet Gateway must be attached to a VPC before it can provide internet connectivity.
- Attaching an Internet Gateway alone does not give resources internet access.
- A Route Table must also include a default route (`0.0.0.0/0`) that points to the Internet Gateway.
- Resources in a public subnet can access the internet only after the Internet Gateway is attached and the Route Table is properly configured.

## Skills Demonstrated

- Amazon VPC
- Internet Gateway (IGW)
- VPC Configuration
- AWS Networking
- Cloud Infrastructure
- AWS Management Console

# Step 6: Create a Route Table

## Objective

The objective of this task was to create a Route Table within my Virtual Private Cloud (VPC). A Route Table controls how network traffic is routed between subnets, the internet, and other AWS resources.

## Steps Performed

1. Logged in to the AWS Management Console.
2. Searched for **VPC** and opened the **VPC Dashboard**.
3. Selected **Route Tables** from the left navigation pane.
4. Clicked **Create route table**.
5. Entered the following details:
   - **Name tag:** My-Route-Table
   - **VPC:** Selected the VPC I had previously created.
6. Clicked **Create route table**.

## Result

The Route Table was successfully created and associated with my VPC. It is now ready to have routing rules added to control how network traffic flows within the VPC and to external networks.

## What I Learned

- A Route Table contains rules, known as routes, that determine where network traffic is directed.
- Every subnet in a VPC must be associated with a Route Table.
- A Route Table can be associated with one or more subnets.
- Creating a Route Table is an important step in enabling communication between resources inside the VPC and external networks such as the internet.

## Skills Demonstrated

- Amazon VPC
- Route Table Configuration
- AWS Networking
- Cloud Infrastructure
- AWS Management Console.# Step 7: Add a Route to the Internet Gateway

## Objective

The objective of this task was to configure the Route Table by adding a default route that directs internet-bound traffic to the Internet Gateway (IGW). This allows resources in the public subnet to communicate with the internet.

## Steps Performed

1. Logged in to the AWS Management Console.
2. Searched for **VPC** and opened the **VPC Dashboard**.
3. Selected **Route Tables** from the left navigation pane.
4. Chose the Route Table I had previously created.
5. Opened the **Routes** tab.
6. Clicked **Edit routes**.
7. Clicked **Add route**.
8. Entered the following values:
   - **Destination:** `0.0.0.0/0`
   - **Target:** Selected the Internet Gateway (IGW) attached to my VPC.
9. Clicked **Save changes**.

## Result

The Route Table was successfully updated with a default route that directs all internet-bound traffic to the Internet Gateway. This configuration enables resources in the associated public subnet to access the internet.

## What I Learned

- A route defines where network traffic should be directed.
- The destination `0.0.0.0/0` represents all IPv4 internet traffic.
- An Internet Gateway must be attached to the VPC before it can be selected as the target for a route.
- A public subnet requires a Route Table with a default route pointing to an Internet Gateway to enable internet connectivity.

## Skills Demonstrated

- Amazon VPC
- Route Table Configuration
- Internet Gateway (IGW)
- VPC Routing
- AWS Networking
- Cloud Infrastructure
- AWS Management Console# Step 7: Add a Route to the Route Table

## Objective

The objective of this task was to add a default route to the Route Table, allowing internet-bound traffic from the public subnet to be directed through the Internet Gateway (IGW). This is an essential step in enabling internet access for resources deployed in the public subnet.

## Steps Performed

1. Logged in to the AWS Management Console.
2. Searched for **VPC** and opened the **VPC Dashboard**.
3. Selected **Route Tables** from the left navigation pane.
4. Chose the Route Table I had previously created.
5. Selected the **Routes** tab.
6. Clicked **Edit routes**.
7. Clicked **Add route**.
8. Entered the following values:
   - **Destination:** `0.0.0.0/0`
   - **Target:** Selected the Internet Gateway (IGW) attached to my VPC.
9. Clicked **Save changes**.

## Result

The Route Table was successfully updated with a default route that directs all internet-bound traffic to the Internet Gateway. This allows resources in the associated public subnet to communicate with the internet.

## What I Learned

- A Route Table contains rules that determine where network traffic is directed.
- The route `0.0.0.0/0` represents all IPv4 internet traffic.
- The Internet Gateway must be attached to the VPC before it can be selected as the route target.
- Without a default route to the Internet Gateway, resources in a public subnet cannot access the internet.

## Skills Demonstrated

- Amazon VPC
- Route Table Configuration
- Internet Gateway (IGW)
- AWS Networking
- Network Routing
- Cloud Infrastructure
- AWS Management Console


# Step 8: Associate the Route Table with the Public Subnet

## Objective

The objective of this task was to associate the Route Table with my public subnet. This ensures that the subnet uses the routing rules defined in the Route Table, allowing resources within the subnet to communicate with the internet through the Internet Gateway.

## Steps Performed

1. Logged in to the AWS Management Console.
2. Searched for **VPC** and opened the **VPC Dashboard**.
3. Selected **Route Tables** from the left navigation pane.
4. Chose the Route Table I had previously created.
5. Selected the **Subnet Associations** tab.
6. Clicked **Edit subnet associations**.
7. Selected my **Public Subnet** from the list of available subnets.
8. Clicked **Save associations**.

## Result

The Route Table was successfully associated with my public subnet. The subnet now uses the routing rules defined in the Route Table, enabling internet connectivity through the attached Internet Gateway.

## What I Learned

- A Route Table must be associated with a subnet before its routing rules take effect.
- Associating a Route Table with a public subnet enables resources in that subnet to use the configured routes.
- For a subnet to be public, it must:
  - Be associated with a Route Table.
  - Have a default route (`0.0.0.0/0`) pointing to an Internet Gateway.
  - Contain resources with public IP addresses (when internet access is required).

## Skills Demonstrated

- Amazon VPC
- Route Table Association
- Public Subnet Configuration
- Internet Gateway Integration
- AWS Networking
- Cloud Infrastructure
- AWS Management Console





