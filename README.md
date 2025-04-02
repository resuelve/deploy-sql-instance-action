# Deploy SQL instance

This action will deploy a SQL instance, or update in case it already exists, for the given parameters.

## Inputs

| Input                  | Required | Description                                                                           |
|------------------------|----------|---------------------------------------------------------------------------------------|
| `working_dir_path`     | yes      | path where the terraform and terragrunt files related to the sql instance are located |
| `terraform_version`    | yes      | Terraform version                                                                     |
| `terragrunt_version`   | yes      | Terragrunt version                                                                    |
| `gcp_credentials_json` | yes      | GCP service account JSON file                                                         |

## Usage

```yaml
- name: Update SQL instance
  uses: resuelve/terragrunt-apply-action@master
    with:
      working_dir_path: live/sandbox/sql-demo
      terraform_version: 1.3.7
      terragrunt_version: 0.55.1
      gcp_credentials_json: ${{ secrets.GCP_CREDENTIALS_JSON }}
```

Enjoy 🎉
