---
# generated by https://github.com/hashicorp/terraform-plugin-docs
page_title: "instaclustr_aws_vpc_peer_v2 Resource - terraform-provider-instaclustr"
subcategory: ""
description: |-
  
---

# instaclustr_aws_vpc_peer_v2 (Resource)



## Example Usage

```terraform
resource "instaclustr_aws_vpc_peer_v2" "myvpcpeer" {
  cdc_id              = "b8129e68-2ee9-4d5e-a29b-74d233b7b4bb"
  peer_aws_account_id = "123456789123"
  peer_vpc_id         = "vpc-aaaa1234"
  peer_subnets        = ["174.16.0.0/20", "172.16.0.0/20", "173.16.0.0/20"]
  peer_region         = "US_EAST_1"
}
```

<!-- schema generated by tfplugindocs -->
## Schema

### Required

- **cdc_id** (String) ID of the Cluster Data Centre
- **peer_aws_account_id** (String) The AWS account ID of the owner of the accepter VPC.
- **peer_region** (String) Region code for the accepter VPC.
- **peer_subnets** (List of String) The subnets for the peering VPC.
- **peer_vpc_id** (String) ID of the VPC with which the peering connection is created.

### Optional

- **id** (String) The ID of this resource.
- **status_code** (String) Status of the VPC Peering Connection. Values can be `pending-acceptance`, `failed`, `expired`, `provisioning`, `active`, `deleting`, `deleted` or `rejected`.
- **timeouts** (Block, Optional) (see [below for nested schema](#nestedblock--timeouts))

<a id="nestedblock--timeouts"></a>
### Nested Schema for `timeouts`

Optional:

- **default** (String)

