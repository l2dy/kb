---
id: OEg9eGdJEwUq6Nb6fXH4p
title: Availability Zones
desc: ''
updated: 1637288555595
created: 1637127947887
---

## Caveats and Gotchas

### Map Availability Zones across accounts

Availability Zone names don't map to the same location across accounts. However, you can use AZ IDs to map Availability Zones across accounts:

1. Open the AWS Resource Access Manager console.
2. In the navigation bar, select your Region from the Region Selector.
3. In the Your AZ ID pane on the right, review the list of Availability Zone names and their corresponding AZ IDs.
    Note: You can also use the `aws ec2 describe-availability-zones --region "region-name"` command in the AWS CLI to generate AZ ID information. Be sure to replace `"region-name"` with the name of your AWS Region.
4. Identify which Availability Zones have the same AZ IDs across your accounts. Availability Zones that have the same AZ IDs map to the same physical location.
