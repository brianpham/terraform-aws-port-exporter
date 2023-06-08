# Port AWS Exporter Module

This Terraform module deploys the Port AWS Exporter in your AWS account.

## Getting Started

To use this module, include the following code in your Terraform configuration:

```terraform
module "port_aws_exporter" {
  source = "git::https://github.com/your/repo.git?ref=initial-project"
  
  stack_name           = var.stack_name
  secret_name          = var.secret_name
  create_bucket        = var.create_bucket
  bucket_name          = var.bucket_name
  config_json_file     = var.config_json_file
  function_name        = var.function_name
}
```

After configuring the module, run the following Terraform commands:

- `terraform init`: Initialize the Terraform configuration.
- `terraform plan --var-file=path/to/variables.tfvars`: Preview the changes to be applied, providing the path to your variables file using the --var-file option.
- `terraform apply --var-file=path/to/variables.tfvars`: Apply the changes and provision the resources in your AWS account, providing the path to your variables file using the --var-file option.
Remember to run `terraform destroy --var-file=path/to/variables.tfvars` to remove the resources when they are no longer needed, providing the path to your variables file using the --var-file option.

Variables
The following variables must be configured for this module:

```
stack_name: (Required) The name of the CloudFormation stack.
secret_name: (Required) The name of the secret for storing credentials.
create_bucket: (Required) Specifies whether to create an S3 bucket.
bucket_name: (Required) The name of the S3 bucket.
config_json_file: (Required) The path to the configuration JSON file.
function_name: (Required) The name of the AWS Lambda function.
Please refer to the module source code or documentation for more information on each variable.
```

To see all possible parameters, see `Variables.tf`.
