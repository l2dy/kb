---
id: gGxHHvt5cp1OH57J4yb08
title: Cloud9
desc: ''
updated: 1639845403106
created: 1639845153868
---

## Caveats and Gotchas

### AWS managed temporary credentials

Some Cloud9, IAM and STS actions are restricted. See [Actions supported by AWS managed temporary credentials](https://docs.aws.amazon.com/cloud9/latest/user-guide/security-iam.html#auth-and-access-control-temporary-managed-credentials-supported).

---

> Currently, if your environment’s EC2 instance is launched into a private subnet, you can't use AWS managed temporary credentials to allow the EC2 environment to access an AWS service on behalf of an AWS entity (an IAM user, for example).

https://docs.aws.amazon.com/cloud9/latest/user-guide/security-iam.html#auth-and-access-control-temporary-managed-credentials
