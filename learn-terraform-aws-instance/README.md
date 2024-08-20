## Important

Make sure to check the `cloud` block in the `main.tf` file for each lab. The `cloud` block is used for Terraform Cloud configurations, and you'll need to adjust it based on your setup.

If you're using **Terraform Cloud**:
- Ensure that you update the `organization` and `workspace` fields to match your Terraform Cloud organization and workspace.

Example:
```hcl
cloud {
  organization = "your-organization"
  workspaces {
    name = "your-workspace"
  }
}
