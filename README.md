# Azure-Networking (Implement and manage virtual networking)

## Azure Virtual Network Setup:
+ Provisioned an Azure Virtual Network (VNet) in a selected region and created multiple subnets (WebApp, Database, Admin) to logically segregate resources.

## On-Premises Network Simulation:
+ Simulated an on-premises environment using a secondary VNet in US West 3.

## Secure Connectivity:

+ Implemented an Azure VPN Gateway to establish a site-to-site VPN between the simulated on-premises VNet and the main Azure VNet. Verified connectivity to enable hybrid communication and configured VNet peering for seamless resource access.

## Resource Deployment

+ Deployed test virtual machines in each subnet, including a CentOS client in the Admin Subnet and a database in the Database Subnet.

## Network Access Control:

+ Configured Network Security Groups (NSGs) to control inbound and outbound traffic, allowing only valid connections—HTTP/HTTPS for WebApp Subnet, MySQL for Database Subnet. Removed public IPs on VMs and implemented an Azure Bastion Host on the admin VNet for secure RDP/SSH access.

## Private Access to Azure PaaS Services:
+ Deployed a MySQL database with custom DNS configuration, and used Azure Load Balancer to distribute traffic internally. Configured an internal load balancer for the database subnet and implemented Azure Private Link to securely access the database over a private endpoint, preventing exposure to the public internet.
