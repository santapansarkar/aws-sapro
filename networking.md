# AWS Networking

**Public service**

Any servive which is having public endpoint. This is not public internet. This is AWS public zone, which is having public endpoint. VPC resources access AWS public zone service without going to public internet. 

**Private service**

Any servive which is inside VPC. If VPC allowed to be accessible from outside then only accessible. 

**DHCP**

Dynamic Host Configuration Protocol. This is used for auto configuration of network resources. Earlier each device has to be updated manually for IP address. Now dhcp server assigns IP address automatically for each devices. Applications running on EC2 instances on subnets can communicate with Amazon DNS server to fetch IP address and other network related informations as needed.  Primary communication need in a local area network are "IP Address","Subnet Mask" and "Gateway Address".

There are two choices in DHCP inside AWS. 

    [1] AmazonProvidedDNS
    [2] CustomDNSDomain

AWS VPC allows dhcp option set to be created. 

DHCP option set is a group of network configurations used by EC2 instances inside VPC to communicate over the virtual network. 




