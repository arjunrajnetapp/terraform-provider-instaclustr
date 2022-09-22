---
page_title: "instaclustr_aws_vpc_peer_v2 Resource - terraform-provider-instaclustr"
subcategory: ""
description: |-
---

# instaclustr_aws_vpc_peer_v2 (Resource)
Definition of an AWS VPC Peering request to allow privately routed connections to a target data centre.
## Example Usage
```
resource "instaclustr_aws_vpc_peer_v2" "example" {
  peer_aws_account_id = "123456789123"
  peer_subnets = [ "10.129.0.0/16" ]
  peer_vpc_id = "vpc-123abc456"
  peer_region = "US_EAST_1"
  cdc_id = "f3eab841-6952-430d-ba90-1bfc3f15da10"
}
```
## Glossary
The following terms are used to describe attributes in the schema of this resource:
- **_read-only_** - These are attributes that can only be read and not provided as an input to the resource.
- **_required_** - These attributes must be provided for the resource to be created.
- **_optional_** - These input attributes can be omitted, and doing so may result in a default value being used.
- **_immutable_** - These are input attributes that cannot be changed after the resource is created.
- **_updatable_** - These input attributes can be updated to a different value if needed, and doing so will trigger an update operation.
- **_nested block_** - These attributes use the [Terraform block syntax](https://www.terraform.io/language/attr-as-blocks) when defined as an input in the Terraform code. Attributes with the type **_repeatable nested block_** are the same except that the nested block can be defined multiple times with varying nested attributes. When reading nested block attributes, an index must be provided when accessing the contents of the nested block, example - `my_resource.nested_block_attribute[0].nested_attribute`.
## Schema
### Input attributes - Required
#### peer_subnets
<ins>Type</ins>: list of strings, required, updatable<br>
<br>The subnets for the peering VPC.
#### cdc_id
<ins>Type</ins>: string (uuid), required, immutable<br>
<br>ID of the Cluster Data Centre
#### peer_region
<ins>Type</ins>: string, required, immutable<br>
<br>Region code for the accepter VPC.
#### peer_vpc_id
<ins>Type</ins>: string, required, immutable<br>
<br>ID of the VPC with which the peering connection is created.
#### peer_aws_account_id
<ins>Type</ins>: string, required, immutable<br>
<br>The AWS account ID of the owner of the accepter VPC.
### Read-only attributes
#### status_code
<ins>Type</ins>: string, read-only<br>
<br>Status of the VPC Peering Connection. Values can be `pending-acceptance`, `failed`, `expired`, `provisioning`, `active`, `deleting`, `deleted` or `rejected`.
#### id
<ins>Type</ins>: string, read-only<br>
<br>ID of the VPC peering connection.
## Import
This resource can be imported using the `terraform import` command as follows:
```
terraform import instaclustr_aws_vpc_peer_v2.[resource-name] "[resource-id]"
```
`[resource-id]` is the unique identifier for this resource matching the value of the `id` attribute defined in the root schema above.
