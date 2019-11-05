# Module Specifics

Core Version Constraints:
* `~> 0.12.2`

Provider Requirements:
* **aws:** `~> 2.16`

## Input Variables
* `account_ids_for_sharing` (required): List of account IDs to allow launch permissions for
* `attributes` (required): Additional attributes (e.g. `1`)
* `client` (required): client, e.g. 'ifunky'
* `delimiter` (default `"-"`): Delimiter to be used between `namespace`, `environment`, `stage`, `name` and `attributes`
* `enabled` (default `true`): Set to false to prevent the module from creating any resources
* `environment` (required): Environment, e.g. 'prod', 'staging', 'dev', 'pre-prod', 'UAT'
* `namespace` (required): Namespace, which could be your organization name or abbreviation, e.g. 'eg' or 'cp'
* `source_ami_id` (required): Unique ID of AMI to copy from source to target region
* `source_ami_name` (required): Unique name of AMI to copy from source to target region
* `source_ami_region` (required): Source AMI region
* `stage` (required): Stage, e.g. 'prod', 'staging', 'dev', OR 'source', 'build', 'test', 'deploy', 'release'
* `tags` (required): Additional tags (e.g. `map('BusinessUnit','XYZ')`

## Output Values
* `ami_id`: ID of copied AMI

## Managed Resources
* `aws_ami_copy.default` from `aws`
* `aws_ami_launch_permission.default` from `aws`

