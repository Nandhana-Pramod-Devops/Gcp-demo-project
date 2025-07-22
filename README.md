<<<<<<< HEAD
# GCP Landing Zone with Terraform

This repository contains Terraform modules and configurations for setting up a secure, scalable, and compliant Google Cloud Platform (GCP) landing zone.

## Directory Structure

```
/0-bootstrap/         # Org-level bootstrap (IAM, billing, groups)
/1-org/              # Org/folder structure
/2-env/              # Environment setup (dev, prod, etc.)
/3-networks/         # Shared VPCs, subnets, firewalls
/4-projects/         # Project creation and configuration
/5-app-infra/        # App-specific infra (GKE, databases, etc.)
/modules/            # Custom/shared Terraform modules
.github/workflows/   # CI/CD for Terraform
```

## Prerequisites

- Terraform >= 1.0.0
- Google Cloud SDK
- Appropriate GCP permissions
- Service account with necessary roles

## Setup Instructions

1. Initialize Terraform:
   ```bash
   terraform init
   ```

2. Configure your variables in `terraform.tfvars`

3. Apply the configuration:
   ```bash
   terraform plan
   terraform apply
   ```

## Module Dependencies

This landing zone uses the following key modules:
- Google Cloud Foundation Fabric (Fabric FAST)
- Custom modules for specific requirements

## Security Considerations

- All infrastructure is deployed with security best practices
- IAM roles follow the principle of least privilege
- Network security is implemented with proper segmentation
- Audit logging is enabled for all resources

## Contributing

1. Fork the repository
2. Create a feature branch
3. Submit a pull request

## License

MIT License 
=======
# Simple Calculator Demo App

A simple Python calculator application designed for SonarQube code quality analysis demonstration.

## Features

- Basic arithmetic operations (add, subtract, multiply, divide, power)
- Calculation history tracking
- Division by zero handling

## Intentional Code Quality Issues

This application contains intentional code quality issues for SonarQube analysis:

1. **Global variables** - `global_var` (bad practice)
2. **Missing type hints** - Function parameters lack type annotations
3. **Unused functions** - `unused_function()` is never called
4. **Unused variables** - `unused_var` in `function_with_issues()`
5. **Hardcoded credentials** - Password in plain text
6. **Magic numbers** - Hardcoded values without constants
7. **Code duplication** - Repeated expressions
8. **Complex functions** - Overly nested loops
9. **Potential security issues** - Division by zero handling

## Running the Application

```bash
python main.py
```

## Running Tests

```bash
pytest test_main.py
```

## SonarQube Analysis

This application is designed to demonstrate various SonarQube code quality checks:

- **Code Smells**: Unused variables, functions, and imports
- **Bugs**: Potential division by zero
- **Vulnerabilities**: Hardcoded passwords
- **Code Coverage**: Test coverage analysis
- **Duplications**: Code duplication detection
- **Complexity**: Cyclomatic complexity analysis

## Expected SonarQube Findings

- Multiple code smells (unused code, magic numbers)
- Security hotspots (hardcoded password)
- Potential bugs (division by zero)
- Code duplications
- High complexity in some functions 
>>>>>>> da284e6f503f9d03aced4fa178342e92196e9644
