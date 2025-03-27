### Virtual Private Cloud (VPC)

* VPC is **your own isolated network** in the cloud
* You have a VPC for each Region
* VPC **spans all the AZ (Subnet)** in that Region
* Multiple VPCs in different Regions
* VPC is like a **virtual representation of network infrastructure**: Server setup, network configuration moved to cloud
> Your resources always have to run in a VPC!

### Subnet
* Subnet is a **range of IP addresses** in your VPC
* It's like a **private network inside a network**.
* You have a subnet for each Availability Zone.

#### Private and Public Subnets
* **Based on firewall configuration** you can have a private and/or public subnet.

* A subnet has a default range of **internal IP addresses**
* When you create a new resource like EC2 instance then an IP
address is assigned within this subnet's IP range
* For **communication inside the VPC**

#### Internet Gateway
* Using an internet gateway you can **connect the VPC** or its subnets to the **outside internet**

### Security - Controlling Access
* Of course you need to **secure your resources**:
    * Control access to your VPC
    * Control access to your individual server instances

#### NACL
* Configure access on **subnet level**

#### Security Group
* Configure access on **instance level**

### CIDR Block
* When you create a subnet, you **specify the IPv4 CIDR block for the subnet**, which is a subset of the VPC CIDR block
* Defines a range of IP addresses
* CIDR = Classless Inter-Domain Routing