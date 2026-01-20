# Shared Workflows

This folder contains shared GitHub Actions workflows for the organization.

Workflows defined here can be reused by organization repositories (`closter-core`, `closter-theme`, etc.) using the `workflow_call` syntax or references to reusable workflows.

## Current Status

Currently no workflows are defined. They will be added as CI/CD and automation requirements are defined for the organization's repositories.

## Proposed Structure

When workflows are defined, they will be organized by purpose:
- `ci/` - Continuous integration workflows
- `cd/` - Continuous deployment workflows
- `automation/` - Automation workflows (dependabot, sync, etc.)

## Usage in Repositories

Individual repositories can reference shared workflows from this repository using the standard GitHub Actions syntax.

