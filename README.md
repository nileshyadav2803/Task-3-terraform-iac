# Task 3 – Infrastructure as Code (IaC) with Terraform

## Overview

This project demonstrates Infrastructure as Code (IaC) using Terraform to provision and manage a local Docker container.

Terraform is used to define the Docker infrastructure as code, while the Docker provider allows Terraform to communicate with the local Docker Engine.

## Objective

The objective of this task is to provision a local Docker container using Terraform and understand the basic Infrastructure as Code workflow.

The project covers:

- Terraform initialization
- Infrastructure planning
- Infrastructure provisioning
- Terraform state inspection
- Docker container verification
- Infrastructure destruction

## Technologies Used

- Terraform
- Docker
- Docker Provider
- Nginx
- Windows
- Visual Studio Code

## Project Structure

```text
Task-3-terraform-iac/
│
├── main.tf
├── execution-logs.txt
├── README.md
└── screenshots/
    ├── 01-terraform-init.png
    ├── 02-terraform-plan.png
    ├── 03-terraform-apply.png
    ├── 04-terraform-state.png
    ├── 05-nginx-browser.png
    └── 06-terraform-destroy.png

Terraform Configuration

The main.tf file defines the Docker infrastructure required for this task.

It includes:

The Docker provider

An Nginx Docker image

An Nginx Docker container

Port mapping from host port 8080 to container port 80


The Docker image is used as the dependency for the Docker container.

Terraform Workflow

1. Initialize Terraform

terraform init

This initializes the Terraform working directory and downloads the required Docker provider.

2. Create an Execution Plan

terraform plan

This previews the infrastructure changes Terraform intends to make without applying them.

Initial result:

Plan: 2 to add, 0 to change, 0 to destroy.

3. Provision the Infrastructure

terraform apply

After confirmation, Terraform provisions the Docker image and Nginx container.

Result:

Apply complete! Resources: 2 added, 0 changed, 0 destroyed.

4. Check Terraform State

terraform state list

The Terraform-managed resources were:

docker_container.nginx
docker_image.nginx

5. Verify the Docker Container

The container was verified using Docker commands.

Container name:

task-3-terraform-nginx

Port mapping:

0.0.0.0:8080 -> 80/tcp

6. Verify the Infrastructure

terraform plan

After provisioning, Terraform reported:

No changes. Your infrastructure matches the configuration.

This confirmed that the infrastructure matched the Terraform configuration.

The Nginx container was also verified through the browser.

7. Destroy the Infrastructure

terraform destroy

The Terraform-managed resources were successfully removed after completing the verification.

Result:

Destroy complete! Resources: 2 destroyed.

Execution Logs

The important Terraform and Docker execution results are documented in:

execution-logs.txt

Key Learning

Through this task, I learned and practiced:

Infrastructure as Code (IaC)

Terraform providers

Terraform resources

Terraform initialization

Terraform planning

Infrastructure provisioning

Terraform state management

Docker container verification

Infrastructure destruction


Conclusion

This project demonstrated how Terraform can be used to define and manage local Docker infrastructure as code.

The complete workflow of initializing, planning, provisioning, verifying, checking state, and destroying infrastructure was successfully performed.

Task Status

Task 3 – Infrastructure as Code (IaC) with Terraform: Completed