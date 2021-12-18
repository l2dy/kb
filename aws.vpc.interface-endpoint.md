---
id: OOqWRZcGGj9J74sJRC88C
title: Interface Endpoint
desc: ''
updated: 1639843628786
created: 1637140383946
---

## Private DNS for interface endpoints

If the private DNS option is enabled, an interface endpoint is created with a hidden private hosted zone attached to the associated VPC. Records in this hosted zone point the default service domain to ENIs of the interface endpoint, which have private IPs that isolated subnets can connect to.

### Caveats and Gotchas

Detach of a private hosted zone can take a few minutes, so it is not possible to recover a deleted AWS service interface endpoint immediately.

API error message:

```
private-dns-enabled cannot be set because there is already a conflicting DNS domain for ssm.<region>.amazonaws.com in the VPC
```
