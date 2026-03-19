---
name: terraform-primer
description: Use when onboarding to a new Terraform project, exploring unfamiliar IaC infrastructure, or needing to understand a Terraform repo's structure, providers, state backend, and module organization
disable-model-invocation: true
---

## Overview
Systematically explores a Terraform project to build a complete understanding of its infrastructure, configuration, and organization.

# Terraform Infrastructure Primer for Claude Code

Use the command `tree` to get an understanding of the Terraform project structure.

Start with reading the CLAUDE.md file if it exists to get context about the infrastructure project.

Read the README.md file to understand the infrastructure purpose and deployment instructions.

Read key Terraform files in order of importance:
1. `versions.tf` or `terraform.tf` - Terraform and provider version constraints
2. `main.tf` - Primary infrastructure definitions
3. `variables.tf` - Input variable definitions
4. `outputs.tf` - Output value definitions
5. `terraform.tfvars.example` or similar example variable files
6. `locals.tf` - Local value definitions (if exists)
7. `data.tf` - Data source definitions (if exists)
8. Any module directories and their key files
9. Environment-specific files (dev.tfvars, prod.tfvars, etc.)

Check for important configuration files:
- `.terraform-version` or `.tool-versions` - Terraform version specification
- `backend.tf` or backend configuration in other files
- `.terraform.lock.hcl` - Provider dependency lock file
- `.gitignore` - Ensure Terraform state files are ignored

Explain back to me:
- Infrastructure purpose and what resources it manages
- Project structure and organization (modules, environments, etc.)
- Key Terraform files and their purposes
- Provider dependencies and versions
- Backend configuration for state management
- Variable structure and required inputs
- Output values and their purposes
- Any environment-specific configurations
- Deployment workflow and important considerations
