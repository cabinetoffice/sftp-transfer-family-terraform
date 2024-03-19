# sscl-atamis-sftp-transfer-family-terraform
Tearraform IaC to create AWS transfer family public sftp

<!--- BEGIN_TF_DOCS --->

## Requirements

| Name | Version |
|------|---------|
| terraform | >= 0.13.0 |

## Providers

| Name | Version |
|------|---------|
| aws | n/a |
| tls | n/a |

## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|------|---------|:--------:|
| account\_name | The account or environment name | `string` | n/a | yes |
| domain\_host | The name of the Route 53 record | `string` | n/a | yes |
| domain\_zone | Hosted Zone name of the desired Hosted Zone | `string` | n/a | yes |
| s3\_bucket\_name | The bucket name | `string` | n/a | yes |
| s3\_bucket\_versioning | Enable bucket versioning | `bool` | n/a | yes |
| security\_policy\_name | Specifies the name of the security policy that is attached to the server. Possible values are TransferSecurityPolicy-2018-11, TransferSecurityPolicy-2020-06, and TransferSecurityPolicy-FIPS-2020-06. Default value is: TransferSecurityPolicy-2018-11. | `string` | `"TransferSecurityPolicy-2018-11"` | no |
| server\_name | Specifies the name of the SFTP server | `string` | n/a | yes |
| sftp\_users | List of SFTP usernames | `list` | `[]` eg `[{username="joe"},{username="john"}]` | yes |

## Outputs

| Name | Description |
|------|-------------|
| endpoint | n/a |

<!--- END_TF_DOCS --->
