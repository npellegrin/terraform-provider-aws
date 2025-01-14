---
subcategory: "EC2 (Elastic Compute Cloud)"
layout: "aws"
page_title: "AWS: aws_ec2_availability_zone_group"
description: |-
  Manages an EC2 Availability Zone Group.
---


<!-- Please do not edit this file, it is generated. -->
# Resource: aws_ec2_availability_zone_group

Manages an EC2 Availability Zone Group, such as updating its opt-in status.

~> **NOTE:** This is an advanced Terraform resource. Terraform will automatically assume management of the EC2 Availability Zone Group without import and perform no actions on removal from configuration.

## Example Usage

```typescript
// Code generated by 'cdktf convert' - Please report bugs at https://cdk.tf/bug
import { Construct } from "constructs";
import { TerraformStack } from "cdktf";
/*
 * Provider bindings are generated by running `cdktf get`.
 * See https://cdk.tf/provider-generation for more details.
 */
import { Ec2AvailabilityZoneGroup } from "./.gen/providers/aws/ec2-availability-zone-group";
class MyConvertedCode extends TerraformStack {
  constructor(scope: Construct, name: string) {
    super(scope, name);
    new Ec2AvailabilityZoneGroup(this, "example", {
      groupName: "us-west-2-lax-1",
      optInStatus: "opted-in",
    });
  }
}

```

## Argument Reference

The following arguments are required:

* `groupName` - (Required) Name of the Availability Zone Group.
* `optInStatus` - (Required) Indicates whether to enable or disable Availability Zone Group. Valid values: `optedIn` or `notOptedIn`.

## Attributes Reference

In addition to all arguments above, the following attributes are exported:

* `id` - Name of the Availability Zone Group.

## Import

EC2 Availability Zone Groups can be imported using the group name, e.g.,

```
$ terraform import aws_ec2_availability_zone_group.example us-west-2-lax-1
```

<!-- cache-key: cdktf-0.17.1 input-ec04450e93feebc7cdb027063eaa1b76316b185dd8882c75d29821697f953592 -->