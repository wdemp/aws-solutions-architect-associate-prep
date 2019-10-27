- VPC endpoint is crucial for private connectivity from your VPC to other AWS services. For example, you can create a VPC endpoint and access S3 from EC2 without going to the internet.
- Each VPC can contain one or more subnet. 
  - Some subnets are connected to the internet via an internet gateway. These are called public subnets. 
  - Private subnets do not have a route to an internet gateway.  
- VPC and Subnet Sizing for IPv4
  - When you create a VPC, you must specify an IPv4 CIDR block for the VPC. The allowed block size is between a /16 netmask (65,536 IP addresses) and /28 netmask (16 IP addresses).
  
- The first four IP addresses and the last IP address in each subnet CIDR block are not available for you to use, and cannot be assigned to an instance. https://docs.aws.amazon.com/vpc/latest/userguide/VPC_Subnets.html
