---
layout: "opentelekomcloud"
page_title: "OpenTelekomCloud: opentelekomcloud_vpc_v2"
sidebar_current: "docs-opentelekomcloud-resource-vpc-v2"
description: |-
  Manages a V2 vpc resource within OpenTelekomCloud.
---

# opentelekomcloud_vpc_v2

Manages a V2 vpc resource within OpenTelekomCloud.

## Example Usage

```hcl
resource "opentelekomcloud_vpc_v2" "resourcevpc" {
  subnet_id = "d9415786-5f1a-428b-b35f-2f1523e146d2"
}
```

## Argument Reference

The following arguments are supported:

* `tenant_id` - (Required) The tenant ID of the operator.

* `vpc_id` - (Required) The VPC ID, which uniquely identifies the VPC.

* `region` - (Optional) The region in which to obtain the V2 Neutron client. A Neutron client is needed to retrieve vpc details from the region. If omitted, the region argument of the provider is used.

* `name` - (Optional) The name of the VPC. The name must be unique for a tenant. The value is a string of no more than 64 characters and can contain digits, letters, underscores (_), and hyphens (-).

* `cidr` - (Optional) The range of available subnets in the VPC. The value must be in CIDR format, for example, 192.168.0.0/16. The value ranges from 10.0.0.0/8 to 10.255.255.0/24, 172.16.0.0/12 to 172.31.255.0/24, or 192.168.0.0/16 to 192.168.255.0/24.

* `routes` - (Optional) The route information.

* `destination` - (Optional) The destination network segment of a route. The value must be in the CIDR format. Currently, only the value 0.0.0.0/0 is supported.

* `nexthop` - (Optional) The next hop of a route. The value must be an IP address and must belong to the subnet in the VPC. Otherwise, this value does not take effect.

* `marker` - (Optional) The resource ID of the pagination query. If the parameter is left empty, only resources on the first page are queried.

* `limit` - (Optional) The number of records returned on each page. The value ranges from 0 to intmax.

  ## Attributes Reference

The following attributes are exported:

* `id` - Specifies a resource ID in UUID format.

* `tenant_id` - See Argument Reference above.

* `vpc_id` - See Argument Reference above.

* `region` - See Argument Reference above.

* `name` -  See Argument Reference above.

* `cidr` - See Argument Reference above.

* `routes` - See Argument Reference above.

* `destination` - See Argument Reference above.

* `nexthop` - See Argument Reference above.

* `marker` - See Argument Reference above.

* `limit` - See Argument Reference above.