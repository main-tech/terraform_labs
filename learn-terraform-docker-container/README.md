## Terraform Docker Example

This Terraform configuration sets up a Docker container running an Nginx web server. It demonstrates how to use Terraform to manage Docker containers.

### Usage

1. Ensure that Terraform and Docker are installed on your local machine.
2. Clone this repository to your local machine.
3. Navigate to the directory containing the Terraform configuration files.
4. Run `terraform init` to initialize the working directory.
5. Run `terraform apply` to apply the Terraform configuration and provision the Docker container.

### Configuration

This Terraform configuration uses the `docker` provider to interact with Docker. It defines a Docker image named "nginx" and a Docker container based on that image. The container is configured to expose port 80 internally and port 8000 externally.



### Providers

In Terraform, a provider is responsible for interacting with APIs to manage resources. Providers are used to abstract the underlying infrastructure and services. In this example, the `docker` provider is used to manage Docker containers and images. It allows Terraform to communicate with the Docker API to create, update, and delete Docker resources.

The Docker provider configuration specifies the source and version of the provider plugin to use:

```hcl
terraform {
  required_providers {
    docker = {
      source  = "kreuzwerker/docker"
      version = "~> 3.0.1"
    }
  }
}

