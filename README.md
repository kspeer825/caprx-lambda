# Pricing Demo Lambda

The following is an example of a lambda function with a publicly accessible url.

Most recent url: https://fkfozxqrk7ybdsfpfsicmxnpem0zflyl.lambda-url.us-west-1.on.aws/

## Dependencies

* Python 3.10
* Terraform 1.7.5

## Usage

Spin up lambda

	export AWS_PROFILE=<your-profile>
	terraform init
	terraform plan apply -auto-approve

The `pricing.py` demo is accessible at the url output. Refresh the page to see pricing generated

	{"price":4432}

Spin down

	terraform plan -destroy -out pricing.tfplan
	terraform apply pricing.tfplan

## Resources

| Name | Type |
|------|------|
| [aws_cloudwatch_log_group.pricing_demo](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/resources/cloudwatch_log_group) | resource |
| [aws_cloudwatch_metric_alarm.pricing_demo_errors](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/resources/cloudwatch_metric_alarm) | resource |
| [aws_iam_role.pricing_demo](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/resources/iam_role) | resource |
| [aws_iam_role_policy_attachment.pricing_demo_eni_attachment](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/resources/iam_role_policy_attachment) | resource |
| [aws_internet_gateway.pricing_demo](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/resources/internet_gateway) | resource |
| [aws_lambda_function.pricing_demo](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/resources/lambda_function) | resource |
| [aws_lambda_function_url.pricing_demo](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/resources/lambda_function_url) | resource |
| [aws_route_table.pricing_demo](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/resources/route_table) | resource |
| [aws_route_table_association.pricing_demo](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/resources/route_table_association) | resource |
| [aws_security_group.pricing_demo](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/resources/security_group) | resource |
| [aws_subnet.pricing_demo](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/resources/subnet) | resource |
| [aws_vpc.pricing_demo](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/resources/vpc) | resource |
| [archive_file.python_lambda_package](https://registry.terraform.io/providers/hashicorp/archive/latest/docs/data-sources/file) | data source |
| [aws_availability_zones.available](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/data-sources/availability_zones) | data source |

## Outputs

| Name | Description |
|------|-------------|
| <a name="output_prcing_demo_url"></a> [prcing\_demo\_url](#output\_prcing\_demo\_url) | n/a |
