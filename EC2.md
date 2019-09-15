AWS EC2 is the primary web sevice that provides resizable compute capacity in the cloud. 
"Compute" refers to the amount of computational power required to fulfill your workload. If your workload is very small, such as websites that recieves few visitors, then yourt compute needd are very small." (aws solutions arichtect associate textbook)
A large workload, such as screening ten million compounds against a comomn cancer target, might require a great deal of compute. 
The amount of compute you might need changes drastically over time.'Insta
Amazon EC2 allows you to acquire compute through the launching of launching virtual servers called "Instances" When you launch an instance, you can make use of the compute as you wish, just as you would with an on-premise server. Because you are paying for the computing power of the instance, you are charged per hour while the instance is running.
When you stop the instance, you are no longer charged. 
There are two concepts that are key to launching instances on AWS(1) the amount of virtual hardware dedicated to the instance (2) the software loaded on the instance. These two dimensions of new instances are controlled, respectively, byu the instance type and the AMI.

INSTANCE Types: There are 4 types of Instances: Virutal CPUs, Memory, Storage, Newtwork performance.

- Instance families:
  -C4: Compute Optimized-For workloads requiring significant processing
  -r3: Memory optimized- For memory-intensive workloads
  -i2: Storage optimized- For workloads requiring high amounts of fast SSD storage
  -g2:GPU-Based instance-intended for graphics and general- purpose GPU  compute workloadso/O )
Many isntances support "enhanced networking" Enhanced networking reduces performance, many instance types support work performance  by enabling a capability called Single Root I/O Virtualization (SR-IOV) 
This results in more PPS (Packets Per Second), lower latency, and less jitter. 
The following instance types support enahnced networking: C3,C4, D2, I2, M4, and R3 families. Part of enabling enhanced networking on an instance you need to make sure the correct drivers are installed and modifying an instance attribute. Enhanced networking is availabe only for these instance launched in an Amazon VPC.

The Amazon Machine Image: defines the initial software that will be on an instance when it's launched. An AMI defines every aspect of the software state at instance launch, includings:
-the OS and its configuration
-initial stae of any patches
-Application or system software
All AMIs are based on x86 OSs, either Linux or Windows.

The 4 Sources of AMI:
-Published by AWS: AWS publishes AMIs with versions of many different OSs, both Linux and Windows. These include multiple distributions of Linux(including Ubuntu , Red Hat, and Amazon's own distribution), Windows 2008, Windows 2012. 
Launching an instance baseds on one of those AMIs will result in the default OS settings, similar to installing an OS from the standard OS ISO image As with any OS installation, you should immediately apply all appropriate patches upon launch.
-AWS Marketplace: The Marketplace is an online store that helps customers find, buy, and immediately start using the software and services that run on EC2. 

## Fault Tolerance
- adding instances in multiple AZs increases fault tolerance
- Use auto scaling groups to provide fault tolerance
-
