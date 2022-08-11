---
# generated by https://github.com/hashicorp/terraform-plugin-docs
page_title: "instaclustr_aws_vpc_peers_v2 Data Source - terraform-provider-instaclustr"
subcategory: ""
description: |-
  
---

# instaclustr_aws_vpc_peers_v2 (Data Source)





<!-- schema generated by tfplugindocs -->
## Schema

### Optional

- **account_id** (String)
- **filter** (Block Set) (see [below for nested schema](#nestedblock--filter))
- **id** (String) The ID of this resource.
- **peering_requests** (Block List) (see [below for nested schema](#nestedblock--peering_requests))

<a id="nestedblock--filter"></a>
### Nested Schema for `filter`

Required:

- **name** (String)
- **values** (List of String)


<a id="nestedblock--peering_requests"></a>
### Nested Schema for `peering_requests`

Optional:

- **cdc_id** (String) ID of the Cluster Data Centre
- **id** (String) ID of the VPC peering connection.
- **peer_aws_account_id** (String) The AWS account ID of the owner of the accepter VPC.
- **peer_region** (String) Region code for the accepter VPC.
- **peer_subnets** (List of String) The subnets for the peering VPC.
- **peer_vpc_id** (String) ID of the VPC with which the peering connection is created.

