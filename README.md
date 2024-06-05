🚀 Step-by- Step Deployment of a 3-Tier Architecture on AWS! 🌐

![aws 3 tier own](https://github.com/FrankNoCoding/A-Simple-AWS-3-Tier-Web-Architecture/assets/110625915/dad26f45-d6e9-4db2-ab54-f429046cd319)


🏗️ Architecture Components:

1.	Virtual Private Cloud (VPC): Created a dedicated VPC for network isolation and control. 

•	Internet Gateway (IGW): Attached to the VPC to enable internet access.
•	NAT Gateway: Configured with an Elastic IP for secure internet access from private instances.

2.	Subnets:

•	Public Subnet: Hosts the Internet Gateway and Load Balancer.
•	Private Subnets: Deployed across multiple availability zones for high availability and security. Hosts the web server and database server in this subnet.

3.	Jump Server:

•	Security Group: Configured to allow secure SSH access to the private instances.

4.	Application Servers:

•	Instances: Two EC2 instances running Apache and PHP, hosted in private subnets.
•	Security Group: Configured to manage traffic to the application servers. Allow Load balancer security group only.
•	PHP Installation: Set up and configured PHP, along with database endpoint additions.

5.	Database Server:

•	Amazon RDS: Running MySQL, deployed in a private subnet for database management and reliability.
•	Security Group: Ensures secure database connections. Allow web server security group only

6.	Load Balancer:

•	Target Group: Configured to include the private instances.
•	Testing: Verified load balancer functionality to ensure optimal fperformance.

🔍 Project Highlights:

•	Security: Implemented strict security group rules and network ACLs.
•	Load Balancer: Depons upon the health check and attributes pass the load to different web servers.
•	High Availability: Multi-AZ deployment for both application and database layers.

