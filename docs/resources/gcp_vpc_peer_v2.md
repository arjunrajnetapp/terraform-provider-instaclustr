---
# generated by https://github.com/hashicorp/terraform-plugin-docs
page_title: "instaclustr_gcp_vpc_peer_v2 Resource - terraform-provider-instaclustr"
subcategory: ""
description: |-
  
---

# instaclustr_gcp_vpc_peer_v2 (Resource)



## Example Usage

```terraform
resource "instaclustr_gcp_vpc_peer_v2" "myvpcpeer" {
  cdc_id                  = "b8129e68-2ee9-4d5e-a29b-74d233b7b4bb"
  peer_project_id         = "example-project123"
  peer_subnets            = ["10.1.0.0/16", "10.2.0.0/16"]
  peer_vpc_network_name   = "network-aabb1122"
}
```

<!-- schema generated by tfplugindocs -->
## Schema

### Required

- **cdc_id** (String) ID of the Cluster Data Centre.
- **peer_project_id** (String) The project ID of the owner of the accepter VPC.
- **peer_subnets** (List of String) The subnets for the peering VPC.
- **peer_vpc_network_name** (String) The name of the VPC Network you wish to peer to.

### Optional

- **failure_reason** (String) Reason for Peering Connection Failure.
- **hidden_property_ignore** (String) This is a hidden property that should be ignored
- **id** (String) The ID of this resource.
- **name** (String) Name of the Peering Connection.
- **status_code** (String) Status of the VPC Peering Connection. Values can be `GENESIS`, `PROVISIONING`, `FAILED`, `INACTIVE`, `ACTIVE` or `UNKNOWN`.
- **timeouts** (Block, Optional) (see [below for nested schema](#nestedblock--timeouts))

<a id="nestedblock--timeouts"></a>
### Nested Schema for `timeouts`

Optional:

- **default** (String)

