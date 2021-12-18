---
id: nu2VmVKOHc95RY9CfadiH
title: ECS
desc: ''
updated: 1639845676621
created: 1639845432503
---

## Caveats and Gotchas

> The `awsvpc` network mode doesn't provide task ENIs with public IP addresses. Therefore, they can’t make direct use of an internet gateway [and therefore can't connect to the internet].

https://docs.aws.amazon.com/AmazonECS/latest/bestpracticesguide/networking-outbound.html
