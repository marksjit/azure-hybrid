# Azure-Networking (Implement and manage virtual networking)

## Azure Virtual Network Setup:
+ Provisioned an Azure Virtual Network (VNet) in chosen region. Created multiple subnets within this VNet to segregate resources effectively (WebApp Subnet, Database Subnet, Admin Subnet).

## On-Premises Network Simulation:
+ For the sake of this project, used another VNet to simulate an on-premises environment. This VNet is located in US West 3.

## Secure Connectivity:

+ Implement Azure VPN Gateway to create a site-to-site VPN connection between your simulated on-premises environment (VNet) and your main Azure VNet. Verify the connection and ensure resources from one VNet can communicate with another, effectively simulating a hybrid environment. For this lab, I implemented a peering connection between the two VNets.

## Resource Deployment

+ Deployed test resources (VMs) in each subnet of main Azure VNet. Deployed a CentOS client VM in the Admin Subnet, a database in the Database Subnet, etc.

## Network Access Control:

+ Created Network Security Groups (NSGs) to define inbound and outbound access rules for Database and WebApp subnet, ensuring that only valid traffic is allowed. For instance, only allow HTTP/HTTPS traffic to the WebApp Subnet and MySQL traffic to the Database Subnet.
+ Removed public IPs on VMs and implemented Azure Bastion Host on VNet02 for secure and seamless RDP and SSH access to virtual machines in the cloud network.

## Private Access to Azure PaaS Services:
+ Deployed a MySQL Database & configure Azure DNS to have custom domain name for your it. Implemented Azure Load Balancer to distribute traffic across resources in the Database Subnet. Deployed internal load balancer on the database subnet.
+ Used Azure Private Link to access MySQL Database over a private endpoint within the VNet, ensuring data doesn't traverse over the public internet.
