# Terraform  AWS VPC Module Customised

This module is going to create the following resources. for HA we are going to get first 2 AZ

* VPC
* Internet Gateway association with VPC
* 2 Public Subnets
* 2 Private Subnets
* 2 Database Subnets
* Databse Subnet groups
* EIP
* NAT Gateway
* Public Route table
* private Route tables
* Database Route table
* Routes
* Route table associations with subnets
* Peering with default VPC(if required)
* Peering routes in acceptor and requeswtor route tables

# Inputs
* project_name (Manadatory) : User must supply their project name
* environment (Manadatory) : User must supply their environment name
* vpc_cidr (Manadatory) : User must supply their vpc_cidr name
* enable_dns_hostnames (optional) : default to true.
* common_tags (optional) : default is empty.  User can supply tagas in list(String) format.
* vpc_tags (optional) : default is empty.  User can supply tagas in list(String) format.
* igw_tags (optional) : default is empty.  User can supply tagas in list(String) format.
* public_subnet_cidrs (Manadatory): User must supplay only 2 valid public subnet CIDR.
* public_subnet_tags (optional) :default is empty.  User can supply tagas in list(String) format.
* private_subnet_cidrs (Manadatory): User must supplay only 2 valid private subnet CIDR.
* private_subnet_tags (optional) :default is empty.  User can supply tagas in list(String) format.
* database_subnet_cidrs (Manadatory): User must supplay only 2 valid database subnet CIDR.
* database_subnet_tags (optional) :default is empty.  User can supply tagas in list(String) format.
* db_subnet_group_tags (optional) :default is empty.  User can supply tagas in list(String) format.
* nat_gateway_tags (optional) :default is empty.  User can supply tagas in list(String) format.
* public_route_table_tags (optional) :default is empty.  User can supply tagas in list(String) format.
* private_route_table_tags (optional) :default is empty.  User can supply tagas in list(String) format.
* database_route_table_tags (optional) :default is empty.  User can supply tagas in list(String) format.
* is_peering_required (optional) :default to false
* aws_vpc_peering_tags (optional) :default is empty.  User can supply tagas in list(String) format.

# Outputs
* vpc_id: VPC ID created.


