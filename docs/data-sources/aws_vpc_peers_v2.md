---
page_title: "instaclustr_aws_vpc_peers_v2 Data Source - terraform-provider-instaclustr"
subcategory: ""
description: |-
---

# instaclustr_aws_vpc_peers_v2 (Data Source)
A listable data source of all AWS VPC Peering requests in an Instaclustr Account.
## Example Usage
```
data "instaclustr_aws_vpc_peers_v2" "example" { }
```
## Glossary
The following terms are used to describe attributes in the schema of this data source:
- **_read-only_** - These are attributes that can only be read and not provided as an input to the data source.
- **_required_** - These attributes must be provided for the data source's information to be queried.
- **_nested block_** - These attributes use the [Terraform block syntax](https://www.terraform.io/language/attr-as-blocks) when defined as an input in the Terraform code. Attributes with the type **_repeatable nested block_** are the same except that the nested block can be defined multiple times with varying nested attributes. When reading nested block attributes, an index must be provided when accessing the contents of the nested block, example - `my_resource.nested_block_attribute[0].nested_attribute`.
## Schema
### Read-only attributes
#### peering_requests
<ins>Type</ins>: repeatable nested block, read-only, see [peering_requests](#nested--peering_requests) for nested schema<br>

#### account_id
<ins>Type</ins>: string, read-only<br>
<br>UUID of the Instaclustr Account.
<a id="nested--peering_requests"></a>
## Nested schema for `peering_requests`

### Read-only attributes
#### peer_subnets
<ins>Type</ins>: list of strings, read-only<br>
<br>The subnets for the peering VPC.
#### cdc_id
<ins>Type</ins>: string (uuid), read-only<br>
<br>ID of the Cluster Data Centre
#### peer_region
<ins>Type</ins>: string, read-only<br>
<br>Region code for the accepter VPC.
#### peer_vpc_id
<ins>Type</ins>: string, read-only<br>
<br>ID of the VPC with which the peering connection is created.
#### id
<ins>Type</ins>: string, read-only<br>
<br>ID of the VPC peering connection.
#### peer_aws_account_id
<ins>Type</ins>: string, read-only<br>
<br>The AWS account ID of the owner of the accepter VPC.
