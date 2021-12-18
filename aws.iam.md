---
id: 3fJLZszwEe9wkgUEys5w4
title: IAM
desc: ''
updated: 1637128352831
created: 1637122971152
---

## Caveats and Gotchas

https://aws.amazon.com/premiumsupport/knowledge-center/iam-increase-policy-size/

### Managed policy limit

You can assign IAM users to up to 10 groups. You can also attach up to 10 managed policies to each group, for a maximum of 120 policies (20 managed policies attached to the IAM user, 10 IAM groups, with 10 policies each).

### Inline policy character quota

You can add as many inline policies as you want to an IAM user, role, or group. But the total aggregate policy size (the sum size of all inline policies) per entity cannot exceed the following quotas:

* User policy size cannot exceed 2,048 characters.
* Role policy size cannot exceed 10,240 characters.
* Group policy size cannot exceed 5,120 characters.
