Create a VPC peer connection, add the two respective VPCs to the connection -> Accept the connection request 
Add a route connection in route table-A by adding CIDR of VPC-B 
Add a route connection in route table-B by adding CIDR of VPC-A
Create an EC2 instance in each of the VPCs, instance-A and instance-B
Go to the security group of instance-A and add an inboud rule of 'All ICMP-IPv4' and CIDR of VPC-B
Go to the security group of instance-B and add an inboud rule of 'All ICMP-IPv4' and CIDR of VPC-A
Connect to instance-A, ping instance-B by using the private IPv4 of instance-B 
Connect to instance-B, ping instance-A by using the private IPv4 of instance-A
If both the ping requests are successful, then the VPC peering is implemented successfully
