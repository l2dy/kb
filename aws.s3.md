---
id: HgYftHkoO7HGJ2SfK6o5K
title: S3
desc: ''
updated: 1637126593506
created: 1637107949076
---

## Caveats and Gotchas

### Partitioning

https://aws.amazon.com/premiumsupport/knowledge-center/s3-prefix-nested-folders-difference/

A prefix is the complete path in front of the object name, which includes the bucket name. For example, if an object (123.txt) is stored as BucketName/Project/WordFiles/123.txt, the prefix is “BucketName/Project/WordFiles/”. If the 123.txt file is saved in a bucket without a specified path, the prefix value is "BucketName/".

A partitioned prefix in a bucket can support 3,500 PUT/COPY/POST/DELETE or 5,500 GET/HEAD requests per second. There is no limit to the number of prefixes you can have in a bucket.

Note: *In Amazon S3, there are no partitions for keys or objects.* Partitions exist only at the prefix level, and not at the object level. For more information about using prefixes in Amazon S3, see Organizing objects using prefixes.
