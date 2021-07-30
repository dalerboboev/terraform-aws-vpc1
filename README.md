# Please copy paste code below
############# Project #############
Amazon Virtual Private Cloud (Amazon VPC) is a service that lets you launch AWS resources in a logically isolated virtual network that you define. You have complete control over your virtual networking environment, including selection of your own IP address range, creation of subnets, and configuration of route tables and network gateways.
By the running below module "vpc1" you will be able build VPC with following configurations:
* 6 subnets: 3 private, 3 public.
* Pulic subnet will attache to the IGW (Internet Gate Way).
* Private subnets will attache to the NAT Gate Way.
* All data present in format based in interpolation architecture (soft coded).

```
module "vpc1" {
  source = "dalerboboev/vpc1/aws"
  region        = "eu-west-2"
  cidr_block    = "10.0.0.0/16"
  public_cidr1  = "10.0.101.0/24"
  public_cidr2  = "10.0.102.0/24"
  public_cidr3  = "10.0.103.0/24"
  private_cidr1 = "10.0.1.0/24"
  private_cidr2 = "10.0.2.0/24"
  private_cidr3 = "10.0.3.0/24"
  tags = {
    Team = "2"
  }
}

```


