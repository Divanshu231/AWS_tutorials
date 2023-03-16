### What is Ec2 ?
Amazon Elastic Compute Cloud (Amazon EC2) provides scalable computing capacity in the Amazon Web Services (AWS) cloud.
Using Amazon EC2 eliminates your need to invest in hardware up front, so you can develop and deploy applications faster. You can use Amazon EC2 
to launch as many or as few virtual servers as you need, configure security and networking, and manage storage.
Amazon EC2 enables you to scale up or down to handle changes in requirements or spikes in popularity, reducing your need to forecast traffic.

### Features of Ec2
 * Amazon Elastic Compute Cloud (Amazon EC2) provides scalable computing
 * capacity in the Amazon Web Services (AWS) cloud.
 * Using Amazon EC2 eliminates your need to invest in hardware up front, so you
 * can develop and deploy applications faster. You can use Amazon EC2 to launch as
 * many or as few virtual servers as you need, configure security and networking, and manage storage.
 * Amazon EC2 enables you to scale up or down to handle changes in requirements or spikes in popularity, reducing your need to forecast traffic.

 There is basic component in data center
Compute
storage
networking
Database
security

Entered into account then you will choose a region
Inconsole you can see all 5 component like that only

Compute
Creating Virtual Machine we can say Servers and in Aws we are saying Instances
Instance Configuration :-
Minimum = 1 CPU = 512 Mb RAM
Max = 128 CPU = 4TB RAM

Types of Instances

* Ondemand Instances :- Where you are not having any upfront cost and no upfront Commitment when you needed you can create and Delete You
will on hourly bases (PPU :- Pay per Usage)

* Spot Instances :- Which will be allocated to you only when the access capacity will be available with the cloud service provider.
When we talking about capacity it means Storage and Ram and Storage is always available ondemand.
so here in spot instances suppose some times the capacity utalization is less from users due to different time zones so that time 
Amazone Rented out those Capacity at 90% Cheaper prices to other users
1. we have to request for these Instances if extra capacity available then only these instances available to you either not
2. These are 90% Cheaper then ondemand 
3. Challenge is These are available max for 6 hours only  
These used in many cases like some companies processes some data they wanted instances for 2 or 3 hour that is the good optionfor them so 
this is the cheaper solutions so Clients and companies waiting for night because this capacity easily available in night and they
requesting for these capacity and then they are doing lot of processes at this perticular time so many of pharmasuitical companies doing 
this

* Reseved Instances :- where you have persistent workload where you need Instances for longer durtion of time
you can take it for 1 years and 3 years because you are making a Commitment for longer duration of time so these instance will be cheaper
to you 

* Scheduled reserved :- If you need the capacity for a perticular schedule suppose your company having seasonal work or you wanted 
servers every saturday or sunday or any day or may be 5 hour in a day according to the work so you can choose this
Minimum you have to take 4 hour in a day 

* Dedicated host :- 
Tenency Model :- Three type of Tenency
1. Shared Tenency :- By Default we are using this
2. Dedicated Tanency :-
3. Dedicated Host :- In in this reserve full Hardware full control of Socket and CPU
BYOL (Bring your own licence) 

Instance type:- According to workload we are choosing the instance type
1. CPU Intensive :- If using OLTP we will be needing more iops due to more request we needed more CPU's in 
compairision to RAM.
2. Memory Intensive :- In this we need more memory just like Ecommerce Website
3. GPU :- like using 3d, Animation, Image processing
4. Storage Intensive:- If you wanted more storage like you wanna create DAS, NAS
5. Big Data workload:- Xlarge 
we are going to these types of optionfor

t :- Cheapest size of instances come in this
C :- Compute 
d :- Database
g :- GPU
i :- big data large type of instances
m :- medium type of utalization (websitehosting)
s :- Storage

AMI :- An Amazon Machine Image (AMI) provides the information required to launch an instance, which is a virtual server in the cloud. 
You specify an AMI when you launch an instance, and you can launch as many instances from the AMI as you need. You can also launch 
instances from as many different AMIs as you need.
An AMI includes the following:
 - A template for the root volume for the instance (for example, an operating system, an application server, and applications)
 - Launch permissions that control which AWS accounts can use the AMI to launch instances
 -  block device mapping that specifies the volumes to attach to the instance when it's launched

If you wanted to deploy the same server in different region so you can create an image and copy AMI to different Region you can create 
just like same server

CHOOSING AN AMI ?
Quick Start: Will give you a bunch of AMI’s which related to most daily used Operating systems AMI’s.
My AMIs: This will give you the list of AMIs which you have taken from the instances.
AWS Marketplace: Will give you a list of AMIs shared by different vendors and third party where you can buy or pay some amount to 
AWS to use those AMI.
Community AMIs: Will give you a list of AMIs which was shared by different communities such as Fedora, Open SUSE, CentOS etc.
Free tier Only: Will display the AMIs which are applicable under Free tier only.

Difference between AMI and template
AMI :- It is precaptured state of OS copy of OS
Copy of OS along with Application 
If you wanted to deploy the same server in different region so you can create an image and copy AMI to different Region you can create 
just like same server 

PIC

Template :- It is  Predefined preconfigured vm copy of VM
Copy of VM along with OS and Application
we can say clone to this.

PIC

### Introduction to Elastic Block Storage(EBS) and Instance Store

• EBS storage is allocated in volumes
o A volume is a 'virtual disk' (size: 1gb – 16tb)
o Basically, a raw block device
o Can be attached to an instance (but only one at a time)
o A single instance can access multiple volumes

• Placed in specific availability zones
o Why is this useful?
o Be sure to place it near instances (otherwise can't attach)

• Replicated across multiple servers
o Data is not lost if a single server fails
o Amazon: Annual failure rate is 0.1-0.2%

Difference between Instance store and EBS
Instance Store :- It is a storage that physically attached to the host computer and cannot be removed. 
Very High IOPS better I/o Performance
If terminate Ec instance loss data automatically
cannot resize the instance store
If physically H/W fails data may be loss
Recommended for
Temporary storage

EBS(Elastic block storage) :- EBS is a storage device(called as a volume) that can be attached to (or removed
from) your instance
Its portable in nature
Data Persistent when the instance is not running
Tied to one AZ
It can only be attached to one instance in the same AZ
EBS Volume is attached like a n/w drive
can be do resize 

Snapshot :-  It is the backup copy of Volume 
If you have any important volume and you dont wanted it deleted accidentally so you can take snapshot of the
volume 


Launch Instance 
LAB









