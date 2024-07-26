---
# generated by https://github.com/hashicorp/terraform-plugin-docs
page_title: "exoscale_block_storage_volume Resource - terraform-provider-exoscale"
subcategory: ""
description: |-
  Manage Exoscale Block Storage https://community.exoscale.com/documentation/block-storage/ Volume.
  Block Storage offers persistent externally attached volumes for your workloads.
---

# exoscale_block_storage_volume (Resource)

Manage [Exoscale Block Storage](https://community.exoscale.com/documentation/block-storage/) Volume.

Block Storage offers persistent externally attached volumes for your workloads.



<!-- schema generated by tfplugindocs -->
## Schema

### Required

- `name` (String) Volume name.
- `zone` (String) ❗ The Exoscale [Zone](https://www.exoscale.com/datacenters/) name.

### Optional

- `labels` (Map of String) Resource labels.
- `size` (Number) Volume size in GB (default 10). If volume is attached, instance must be stopped to update this value. Volume can only grow, cannot be shrunk.
- `snapshot_target` (Attributes) Block storage snapshot to use when creating a volume. Read-only after creation. (see [below for nested schema](#nestedatt--snapshot_target))
- `timeouts` (Block, Optional) (see [below for nested schema](#nestedblock--timeouts))

### Read-Only

- `blocksize` (Number) Volume block size.
- `created_at` (String) Volume creation date.
- `id` (String) The ID of this resource.
- `state` (String) Volume state.

<a id="nestedatt--snapshot_target"></a>
### Nested Schema for `snapshot_target`

Optional:

- `id` (String) Snapshot ID.


<a id="nestedblock--timeouts"></a>
### Nested Schema for `timeouts`

Optional:

- `read` (String) A string that can be [parsed as a duration](https://pkg.go.dev/time#ParseDuration) consisting of numbers and unit suffixes, such as "30s" or "2h45m". Valid time units are "s" (seconds), "m" (minutes), "h" (hours). Read operations occur during any refresh or planning operation when refresh is enabled.

-> The symbol ❗ in an attribute indicates that modifying it, will force the creation of a new resource.

