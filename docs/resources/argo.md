---
page_title: "cloudflare_argo Resource - Cloudflare"
subcategory: ""
description: |-
  Cloudflare Argo controls the routing to your origin and tiered
  caching options to speed up your website browsing experience.
---

# cloudflare_argo (Resource)

Cloudflare Argo controls the routing to your origin and tiered
caching options to speed up your website browsing experience.

## Example Usage

```terraform
resource "cloudflare_argo" "example" {
  zone_id        = "0da42c8d2132a9ddaf714f9e7c920711"
  tiered_caching = "on"
  smart_routing  = "on"
}
```
<!-- schema generated by tfplugindocs -->
## Schema

### Required

- `zone_id` (String) The zone identifier to target for the resource.

### Optional

- `smart_routing` (String) Whether smart routing is enabled. Available values: `on`, `off`.
- `tiered_caching` (String) Whether tiered caching is enabled. Available values: `on`, `off`.

### Read-Only

- `id` (String) The ID of this resource.

## Import

Import is supported using the following syntax:
```shell
$ terraform import cloudflare_argo.example <zone_id>
```
