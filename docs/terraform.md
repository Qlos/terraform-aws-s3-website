<!-- BEGIN_TF_DOCS -->
## Documentation


### Requirements

| Name | Version |
|------|---------|
| <a name="requirement_terraform"></a> [terraform](#requirement\_terraform) | >= 0.14 |
| <a name="requirement_aws"></a> [aws](#requirement\_aws) | >= 2.0.0 |

### Modules

| Name | Source | Version |
|------|--------|---------|
| <a name="module_website_bucket"></a> [website\_bucket](#module\_website\_bucket) | Infrastrukturait/s3-bucket/aws | 0.1.0 |

### Resources

| Name | Type |
|------|------|
| [aws_cloudfront_distribution.website_cdn](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/resources/cloudfront_distribution) | resource |
| [aws_cloudfront_origin_access_identity.origin_access_identity](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/resources/cloudfront_origin_access_identity) | resource |
| [aws_iam_policy_document.s3_policy](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/data-sources/iam_policy_document) | data source |

### Inputs

| Name | Description | Type | Default | Required |
|------|-------------|------|---------|:--------:|
| <a name="input_acm_certificate_arn"></a> [acm\_certificate\_arn](#input\_acm\_certificate\_arn) | n/a | `string` | `""` | no |
| <a name="input_block_public_acls"></a> [block\_public\_acls](#input\_block\_public\_acls) | Enable block public ACLs on S3 bucket | `bool` | `true` | no |
| <a name="input_block_public_policy"></a> [block\_public\_policy](#input\_block\_public\_policy) | Enable block public access on S3 bucket | `bool` | `true` | no |
| <a name="input_bucket_name"></a> [bucket\_name](#input\_bucket\_name) | The name of the S3 bucket to create. | `string` | n/a | yes |
| <a name="input_default_root_object"></a> [default\_root\_object](#input\_default\_root\_object) | The object that you want CloudFront to return (for example, index.html) when an end user requests the root URL. | `string` | `"index.html"` | no |
| <a name="input_domain"></a> [domain](#input\_domain) | n/a | `string` | n/a | yes |
| <a name="input_ipv6"></a> [ipv6](#input\_ipv6) | Enable IPv6 on CloudFront distribution | `bool` | `false` | no |
| <a name="input_minimum_client_tls_protocol_version"></a> [minimum\_client\_tls\_protocol\_version](#input\_minimum\_client\_tls\_protocol\_version) | CloudFront viewer certificate minimum protocol version | `string` | `"TLSv1.2_2021"` | no |
| <a name="input_not_found_response_code"></a> [not\_found\_response\_code](#input\_not\_found\_response\_code) | The HTTP status code that you want CloudFront to return with the custom error page to the viewer. | `string` | `"404"` | no |
| <a name="input_not_found_response_path"></a> [not\_found\_response\_path](#input\_not\_found\_response\_path) | The path of the custom error page (for example, /custom\_404.html). | `string` | `"/404.html"` | no |
| <a name="input_price_class"></a> [price\_class](#input\_price\_class) | CloudFront price class | `string` | `"PriceClass_200"` | no |
| <a name="input_routing_rules"></a> [routing\_rules](#input\_routing\_rules) | n/a | `string` | `""` | no |
| <a name="input_tags"></a> [tags](#input\_tags) | Tags map for resources | `map(string)` | `{}` | no |

### Outputs

| Name | Description |
|------|-------------|
| <a name="output_website_bucket_arn"></a> [website\_bucket\_arn](#output\_website\_bucket\_arn) | n/a |
| <a name="output_website_bucket_id"></a> [website\_bucket\_id](#output\_website\_bucket\_id) | n/a |
| <a name="output_website_cdn_arn"></a> [website\_cdn\_arn](#output\_website\_cdn\_arn) | n/a |
| <a name="output_website_cdn_hostname"></a> [website\_cdn\_hostname](#output\_website\_cdn\_hostname) | n/a |
| <a name="output_website_cdn_id"></a> [website\_cdn\_id](#output\_website\_cdn\_id) | n/a |
| <a name="output_website_cdn_zone_id"></a> [website\_cdn\_zone\_id](#output\_website\_cdn\_zone\_id) | n/a |

<!-- END_TF_DOCS -->