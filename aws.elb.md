---
id: 63nWmVsSwFrZPwhCicDql
title: ELB
desc: ''
updated: 1639843158911
created: 1637111390081
---

# Elastic Load Balancing

## Caveats and Gotchas

### Security groups

https://aws.amazon.com/premiumsupport/knowledge-center/security-group-load-balancer/

If you're using an Application Load Balancer, follow the instructions at Security groups for your Application Load Balancer.

If you're using a Network Load Balancer, update the security groups for your target instances because Network Load Balancers don't have associated security groups.

* If your target type is an IP, add a rule to your security group to allow traffic from your load balancer's IP address to the target IP address.
* If your target type is an instance, add a rule to your security group to allow traffic from your load balancer's IP address and clients to the target IP address.
