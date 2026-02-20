-----Architecture Flow-----



-----AWS Resources Created-----

i)    VPC
ii)   2 Public Subnets
iii)  2 Private Subnets
iv)   Internet Gateway
v)    NAT Gateway
vi)   Route Tables
vii)  2 EC2 Instances (t2.micro)
viii) Application Load Balancer
ix)   Target Group
x)   Security Groups


-----Deployment Steps-----

1. Create VPC
CIDR: 10.0.0.0/16
2 Public Subnets
2 Private Subnets

2. Configure Gateways
Attach Internet Gateway to VPC
Create NAT Gateway in public subnet
Update route tables

3. Launch EC2 Instances
AMI: Amazon Linux 2023
Type: t2.micro
Deploy in private subnets
No public IP
Use Bastion host

4. Install Nginx

```bash
sudo yum install nginx -y
sudo systemctl start nginx
sudo systemctl enable nginx
