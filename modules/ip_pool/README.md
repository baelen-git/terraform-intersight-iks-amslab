# ip_pool - Intersight IP Pool Terraform Module

## Usage

```hcl
module "ip_pool" {

  source = "terraform-cisco-modules/iks/intersight//modules/ip_pool"

  # omitted...
}
```

This module will deploy an IP Pool Policy within Intersight.  This can be used to create IKS clusters or other objects that require an IP Pool.  

* This sub-module will be moved into a different module repository at a future date.


These resources are created

* [ippool](https://registry.terraform.io/providers/CiscoDevNet/intersight/latest/docs/resources/ippool_pool)

<!-- BEGINNING OF PRE-COMMIT-TERRAFORM DOCS HOOK -->
## Requirements

| Name | Version |
|------|---------|
| terraform | >= 0.14.5 |
| intersight | =1.0.0 |

## Providers

| Name | Version |
|------|---------|
| intersight | =1.0.0 |

## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|------|---------|:--------:|
| gateway | Default gateway for this pool. | `string` | n/a | yes |
| name | Name of the IP Pool to be created. | `string` | n/a | yes |
| netmask | Subnet Mask for this pool. | `string` | n/a | yes |
| org\_name | Intersight Organization name | `string` | n/a | yes |
| pool\_size | Number of IPs you want this pool to contain. | `string` | n/a | yes |
| primary\_dns | Primary DNS Server for this pool. | `string` | n/a | yes |
| secondary\_dns | Secondary DNS Server for this pool. | `string` | n/a | yes |
| starting\_address | Starting IP Address you want for this pool. | `string` | n/a | yes |
| tags | n/a | `list(map(string))` | `[]` | no |

## Outputs

No output.

<!-- END OF PRE-COMMIT-TERRAFORM DOCS HOOK -->