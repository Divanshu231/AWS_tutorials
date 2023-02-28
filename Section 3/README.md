### What is a VPC (Virtual Private Cloud)
A virtual private cloud (VPC) is a virtual network that closely resembles a traditional network that you'd 
operate in your own data centre, with the benefits of using the scalable infrastructure of Amazon Web Services(AWS).
Amazon Virtual Private Cloud (Amazon VPC) enables you to launch Amazon Web Services (AWS) resources into a
virtual network that you've defined.
You can create isolated networks for your applications or clients.
VPC: A virtual private cloud (VPC) is a virtual network dedicated to your AWS account. It is logically 
isolated from other virtual networks in the AWS cloud. You can launch your AWS resources, such as Amazon
EC2 instances, into your VPC. You can configure your VPC; you can select its IP address range, create subnets,
and configure route tables, network gateways, and security settings.

Subnet: A subnet is a range of IP addresses in your VPC. You can launch AWS resources into a subnet that you 
select. Use a public subnet for resources that must be connected to the Internet, and a private subnet for 
resources that won't be connected to the Internet.

Route Table: A route table contains a set of rules, called routes, that are used to determine where network traffic is directed.
Each subnet in your VPC must be associated with a route table; the table controls the routing for the subnet. A subnet can only be associated with one route table at a time, but you can associate multiple subnets with the same route table.

Internet Gateway: An Internet gateway is a horizontally scaled, redundant, and highly available VPC component that allows communication between instances in your VPC and the Internet. It therefore imposes no availability risks or bandwidth constraints on your network traffic.
An Internet gateway serves two purposes: to provide a target in your VPC route tables for Internet-routable traffic, and to perform network address translation (NAT) for instances that have been assigned public IP addresses.

Network ACLs: A network access control list (ACL) is an optional layer of security for your VPC that acts as a firewall for controlling traffic in and out of one or more subnets. You might set up network ACLs with rules similar to your security groups in order to add an additional layer of security to your VPC.



### Security in Your VPC
Amazon VPC provides three features that you can use to increase and monitor the security for your VPC:
Security groups: Act as a firewall for associated Amazon EC2 instances, controlling both inbound and outbound traffic at the instance level
Network access control lists (ACLs): Act as a firewall for associated subnets, controlling both inbound and outbound traffic at the subnet level
Flow logs: Capture information about the IP traffic going to and from network interfaces in your VPC

### VPC Architecture and Internal working of VPC

Pic

Design and Deploy Virtual Private Cloud.
Create Subnets, Internet gateway, Routing, Security Groups and deploy EC2 machine
with Key Pair.
through Video