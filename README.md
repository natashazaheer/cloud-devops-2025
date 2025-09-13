Project Overview

This project sets up a basic Cloud-DevOps environment using AWS, Terraform, Ansible, Docker, and Docker Compose. The work covers infrastructure provisioning, server configuration, and installation of key DevOps tools.

Project Structure
terraform/        → Terraform configuration files for AWS infrastructure
ansible/          → Ansible playbook for server provisioning
docker/           → Flask application, Dockerfile, requirements.txt
docker-compose/   → Docker Compose configuration for services


Steps Completed
1. Infrastructure Setup (Terraform)

Created a custom VPC with public and private subnets.

Configured Internet Gateway and NAT Gateway.

Added security groups for bastion and application servers.

Provisioned a bastion host for SSH access and a private application server.

Enabled remote state storage in AWS S3 with DynamoDB for state locking.

2. Server Provisioning (Ansible)

Automated installation of Docker and Docker Compose.

Configured user permissions for running Docker-based services.

3. Containerized Services (Docker & Docker Compose)

Deployed services via docker-compose.yml:

Jenkins (LTS version).

PostgreSQL database for SonarQube.

SonarQube connected to PostgreSQL.

Grafana and Prometheus (defined in Compose, setup in progress).

