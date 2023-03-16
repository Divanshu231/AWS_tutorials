### What is a Security Group(SG)?
A security group acts as a virtual firewall that controls the traffic for one or more instances.
When you launch an instance, you associate one or more security groups with the instance.
You add rules to each security group that allow traffic to or from its associated instances.
You can modify the rules for a security group at any time; the new rules are automatically applied 
to all instances that are associated with the security group.
Its Just like a software firwell as you know Every OS having a Software firewall like that SG is a 
software firewall.
In Security Groups we are having Inbound and Outbound rules
Inbound rules :- We are filtering Inbound
Eg:- SSH - 22
rdp :- 3389
http :- 80
Outbound rules :- All traffic is allowed by Default 
NOTE :- Each and Every resource in aws is protected by the security group by default.

### What is Network Access Control List (NACL)?

Network access control lists (ACLs): Act as a firewall for associated subnets, controlling both inbound and outbound traffic at the subnet level.

Components of NACL

Following are the components of Network Access Control List (NACL): 

    Rule number: Every rule is assigned a unique number. The rule’s priority is also based on the number it is assigned. When it matches to a specific request or traffic, this rule is applied to the request, irrespective of whether another high-numbered rule contradicts it or not.  

Rules are created with specific increments, like the difference between 2 rules is either 1,10, 100 and all the rules created have this same difference.  

    Type: This tells about the type of traffic, like SSH, HTTP, HTTPS.  
    Protocol: Protocol is a set of rules, that is applied to every request, ex: http, https, ICMP, SSH. 
    Portrange: The listening port, which takes in the request from the user, such as HTTP is associated with port 80.  
    Inboundrules: Also known as source. These rules talk about the source from where the request or traffic is coming from, and about the destination port/ the port through which the response is sent.  
    Outboundrules: Also known as destination. These rules talk about where the response should be sent and about the destination port.  
    Allow/Deny: Whether the specific traffic has to be allowed or denied.  

### Differentiate SG vs NACL?
Security Group
1) It supports only allow rules, and by default, all the rules are denied. You    cannot deny the rule for establishing a connection.
2) It is a stateful means that any changes made in the inbound rule will be    automatically reflected in the outbound rule. For example, If you are      allowing an incoming port 80, then you also have to add the outbound rule      explicitly.
3) It is associated with an EC2 instance.
4) All the rules are evaluated before deciding whether to allow the traffic.
5) Security Group is applied to an instance only when you specify a security    group while launching an instance.
6) It is the first layer of defense.
NACL
1) It supports both allow and deny rules, and by default, all the rules are    denied. You need to add the rule which you can either allow or deny it.
2) It is a stateless means that any changes made in the inbound rule will not    reflect the outbound rule, i.e., you need to add the outbound rule    separately. For example, if you add an inbound rule port number 80, then you    also have to explicitly add the outbound rule.
3) It is associated with a subnet.
4) Rules are evaluated in order, starting from the lowest number.
5) NACL has applied automatically to all the instances which are associated    with an instance.
6) It is the second layer of defense.



