---
subcategory: "Transit Gateway"
layout: "aws"
page_title: "AWS: aws_ec2_transit_gateway_dx_gateway_attachment"
description: |-
  Get information on an EC2 Transit Gateway's attachment to a Direct Connect Gateway
---


<!-- Please do not edit this file, it is generated. -->
# Data Source: aws_ec2_transit_gateway_dx_gateway_attachment

Get information on an EC2 Transit Gateway's attachment to a Direct Connect Gateway.

## Example Usage

### By Transit Gateway and Direct Connect Gateway Identifiers

```typescript
// Code generated by 'cdktf convert' - Please report bugs at https://cdk.tf/bug
import { Construct } from "constructs";
import { Token, TerraformStack } from "cdktf";
/*
 * Provider bindings are generated by running `cdktf get`.
 * See https://cdk.tf/provider-generation for more details.
 */
import { DataAwsEc2TransitGatewayDxGatewayAttachment } from "./.gen/providers/aws/data-aws-ec2-transit-gateway-dx-gateway-attachment";
class MyConvertedCode extends TerraformStack {
  constructor(scope: Construct, name: string) {
    super(scope, name);
    new DataAwsEc2TransitGatewayDxGatewayAttachment(this, "example", {
      dxGatewayId: Token.asString(awsDxGatewayExample.id),
      transitGatewayId: Token.asString(awsEc2TransitGatewayExample.id),
    });
  }
}

```

## Argument Reference

The following arguments are supported:

* `transitGatewayId` - (Optional) Identifier of the EC2 Transit Gateway.
* `dxGatewayId` - (Optional) Identifier of the Direct Connect Gateway.
* `filter` - (Optional) Configuration block(s) for filtering. Detailed below.
* `tags` - (Optional) Map of tags, each pair of which must exactly match a pair on the desired Transit Gateway Direct Connect Gateway Attachment.

### filter Configuration Block

The following arguments are supported by the `filter` configuration block:

* `name` - (Required) Name of the filter field. Valid values can be found in the [EC2 DescribeTransitGatewayAttachments API Reference](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_DescribeTransitGatewayAttachments.html).
* `values` - (Required) Set of values that are accepted for the given filter field. Results will be selected if any given value matches.

## Attribute Reference

In addition to all arguments above, the following attributes are exported:

* `id` - EC2 Transit Gateway Attachment identifier
* `tags` - Key-value tags for the EC2 Transit Gateway Attachment

## Timeouts

[Configuration options](https://developer.hashicorp.com/terraform/language/resources/syntax#operation-timeouts):

- `read` - (Default `20M`)

<!-- cache-key: cdktf-0.17.1 input-24342787a3ce635e686cc7f106a91787a880dd41a77e294e579c6c74e8174823 -->