# VPC

## VPC flow logs

network traffic -> Flow logs -> Amazon CLoudWatch logs -> stream Lambda/ElasticSearch service

### Levels
* VCP
* Subnet
* Network interface level

Exam tips:
* no flow logs for VPCs that are peered with your VPC unless the peer VCP in in your account
* no tags
* can't change configuration
* no DNS/win licesnse/metadata traffic/DHCP traffic/traffic to the reserved IP address for the default VCP router

## VPC endpoints

internal gateway to AWS services

Interface vs gateway (HA) endpoint

## Summary

- NAT instance throughput depends on instance size
- NAT gw scales up to 10Gbps, no need to patch, more secure that NAT instances
- NACL by default denies all inboud and outbound traffic
- NACL -> multiple sbunets, subnet -> only one NACL
- NACL are stateless