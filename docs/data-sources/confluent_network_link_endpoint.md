---
# generated by https://github.com/hashicorp/terraform-plugin-docs
page_title: "confluent_network_link_endpoint Data Source - terraform-provider-confluent"
subcategory: ""
description: |-
   
---

# confluent_network_link_endpoint Data Source

[![Early Access](https://img.shields.io/badge/Lifecycle%20Stage-Early%20Access-%2300afba)](https://docs.confluent.io/cloud/current/api.html#section/Versioning/API-Lifecycle-Policy)

-> **Note:** `confluent_network_link_endpoint` data source is available in **Early Access** for early adopters. Early Access features are introduced to gather customer feedback. This feature should be used only for evaluation and non-production testing purposes or to provide feedback to Confluent, particularly as it becomes more widely available in follow-on editions.  
**Early Access** features are intended for evaluation use in development and testing environments only, and not for production use. The warranty, SLA, and Support Services provisions of your agreement with Confluent do not apply to Early Access features. Early Access features are considered to be a Proof of Concept as defined in the Confluent Cloud Terms of Service. Confluent may discontinue providing Early Access releases of the Early Access features at any time in Confluent’s sole discretion.

`confluent_network_link_endpoint` describes a Network Link Endpoint data source.

## Example Usage

```terraform
data "confluent_network_link_endpoint" "nle" {
  id = "nle-1357"
  environment {
    id = "env-1234"
  }
}

output "network_link_endpoint" {
  value = data.confluent_network_link_endpoint.nle
}
```

<!-- schema generated by tfplugindocs -->
## Argument Reference

The following arguments are supported:

- `id` - (Required String) The ID of the Network Link Endpoint, for example, `nle-zyw30`.
- `environment` (Required Configuration Block) supports the following:
  - `id` - (Required String) The ID of the Environment that the Network Link Endpoint belongs to, for example, `env-xyz456`.

## Attributes Reference

In addition to the preceding arguments, the following attributes are exported:

- `display_name` - (Optional String) The name of the Network Link Endpoint.
- `description` - (Optional String) The description of the Network Link Endpoint.
- `network` (Required Configuration Block) supports the following:
  - `id` - (Required String) The ID of the Network that the Network Link Endpoint belongs to, for example, `n-abc123`.
- `network_link_service` (Required Configuration Block) supports the following:
  - `id` - (Required String) The ID of the Network Link Service
- `resource_name` (Required String) The Confluent Resource Name of the Network Link Endpoint.