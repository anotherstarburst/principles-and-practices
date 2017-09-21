---
layout: page
title: Conventions
---

## Paths and keys

Where we need to construct a path or a key, for example for directory structure or S3 keys we should use the following convention:

```
<environment/account>/<country>/<product>/<stage>/<service>
```

### Examples



### Environments

The environments are:

* production
* staging
* qa
* development

### Accounts

The AWS accounts are:

* production
* staging
* main

### Countries

In general this is either the `uk` or `us` depending on the business or legal entity that is operating in the infrastructure.

For datastores the country and the AWS region should definitely match. For other infrastructure where data is not at rest it may not matter as much.

### Products

Product names are things like `crew-portal`, `photoshoot`, `popsss`, etc.

### Stage

The stages are:

* production
* staging
* qa
* development

Note: where the stage is the same as the account or environment there is no need to duplicate the stage in the key value.

### Services

These are generally AWS service names such as `s3` or `iam`.