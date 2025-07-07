# Governance Scripts 🛡️

Reusable snippets for tagging, pruning, cost-hygiene, security scanning, and signing tasks in Azure-style environments.

## Current Features

*   **Trivy Image Scanning**: Builds Docker images, scans them for vulnerabilities using Trivy, and uploads the scan report as a SARIF artifact.  Images are saved as artifacts when the scan succeeds. Implemented using the `.github/workflows/trivy-scan.yml` workflow.
*   **Sigstore Signing**: Signs container images using Sigstore/Cosign and uploads the signature to Rekor. Implemented using the `.github/workflows/sigstore-sign.yml` workflow.

## Usage

This repository provides reusable GitHub Actions workflows for common governance tasks. See the individual workflow files in the `.github/workflows/` directory for details on their inputs, secrets, and usage.

*   **.github/workflows/trivy-scan.yml**:  To use this workflow, you must provide the `service-name`, `service-context-path`, and `image-name` as inputs. Also, you must provide `GH_TOKEN` as a secret.
*   **.github/workflows/sigstore-sign.yml**:  To use this workflow, you must provide the `image-digest` as an input.  Also, you must provide `GH_TOKEN` as a secret.

## Planned Features

*   Enhanced Tagging and Pruning capabilities
*   More comprehensive RBAC auditing

## Contributing

> See **open issues** for discussion and contribution guidelines.
