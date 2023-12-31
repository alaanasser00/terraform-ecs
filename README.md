﻿## Deploy an AWS ECS Cluster with Terraform

This repository contains Terraform files to deploy an AWS ECS cluster. The ECS cluster orchestrates containerized applications, offering scalability and ease of management.

### Prerequisites

Before executing the Terraform files, ensure you have:

- An AWS account
- AWS CLI configured with appropriate permissions
- Terraform installed locally

### Getting Started

1. **Clone the Repository:**
    ```bash
    git clone https://github.com/crc-aws/ecs-app.git
    cd your-repo
    ```

2. **Set up AWS Credentials:**
    Ensure your AWS credentials are properly configured. You can use `aws configure` or set environment variables (`AWS_ACCESS_KEY_ID`, `AWS_SECRET_ACCESS_KEY`, `AWS_REGION`).

3. **Update Configuration:**
    Modify the `main.tf` file:
    - Enter your AWS Account ID in the execution role ARN.

4. **Deploy the ECS Cluster:**
    Execute the following commands:
    ```bash
    terraform init
    terraform apply
    ```

### Configuration Details

- `provider.tf`: Holds the Terraform setup for configuring the Terraform provider.
- `main.tf`: Manages the Terraform configuration to establish an ECS cluster.
- `ec2.tf`: Governs the Terraform configuration for creating EC2 instances.
- `vpc.tf`: Handles the Terraform setup for establishing the VPC.
- `variables.tf`: Defines variables utilized throughout the Terraform configuration.

### Maintenance

Remember to destroy the resources when they are no longer needed:
```bash
terraform destroy
```

### Contributing

Contributions are welcome! Feel free to submit issues or pull requests.

### Acknowledgments

Special thanks to Sumeet Ninawe's [article](https://spacelift.io/blog/terraform-ecs) for inspiration. You can also explore the original repository [here](https://github.com/sumeetninawe/ecsec2/tree/main)

---

Feel free to tailor this template further based on specifics about your project, including adding sections about usage, troubleshooting, or any other relevant information that might assist users in understanding and utilizing your repository.
