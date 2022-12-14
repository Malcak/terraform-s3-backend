# Terraform S3 Backend Module
### Example
```hcl
data "aws_iam_account_alias" "alias" {}

module "backend" {
  source = "github.com/Malcak/terraform-s3-backend.git"
  bucket_purpose = "${var.project}-${var.environment}"
  accout_alias = "${data.aws_iam_account_alias.alias}"
  region = "${var.region}"
}
```