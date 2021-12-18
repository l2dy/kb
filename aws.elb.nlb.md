---
id: vX07y4hKEMwMvuFq8WBkO
title: NLB
desc: ''
updated: 1639844780260
created: 1639842595770
---

## Caveats and Gotchas

> You cannot change the health check interval for a target group with the TCP protocol.

---

Quoting AWS Support:

> When you register a new target to your Network Load Balancer, it is expected to take between 90 and 180 seconds to complete the registration process. After registration is complete, the Network Load Balancer health check systems will begin to send health checks to the target. A newly registered target must pass health checks for the configured interval to enter service and receive traffic. For example, if you configure your health check for a 30 second interval, and require 3 health checks to become healthy, the minimum time a newly registered target could enter service is 90 seconds after a new target passes its first health check.
>
> Similarly, when you deregister a target from your Network Load Balancer, it is expected to take 90-180 seconds to process the requested deregistration, after which it will no longer receive new connections. During this time the Elastic Load Balancing API will report the target in 'draining' state. The target will continue to receive new connections until the deregistration processing has completed. At the end of the configured deregistration delay, the target will not be included in the describe-target-health response for the Target Group, and will return 'unused' with reason 'Target.NotRegistered' when querying for the specific target.

https://stackoverflow.com/a/67203212 (CC BY-SA 4.0)

---

> There is a limit on the number of ALBs, CLBs and NLBs per region (separately). As of late 2017, the default limit for each is 20 per region. These limits can be easily raised for ALB and CLB, but AWS is quite reluctant to raise the limit on NLBs.

https://github.com/open-guides/og-aws#load-balancer-gotchas-and-limitations (CC BY-SA 4.0)
