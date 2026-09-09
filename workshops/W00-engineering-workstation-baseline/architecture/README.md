# W00 Workstation Architecture

## Target Principle

Windows provides host and desktop integration.

WSL2 Ubuntu provides the primary Linux engineering environment.

## Windows-hosted components

- VS Code GUI
- Docker Desktop
- Browser
- WSL2 platform

## WSL2 Ubuntu components

- Bash
- Git
- Python / pip / venv
- Node.js / npm
- Azure CLI
- GitHub CLI
- Terraform
- jq / yq
- SSH / curl
- Docker CLI

## Intended Integrations

- VS Code on Windows connects into WSL.
- Docker CLI in WSL communicates with Docker Desktop.
- Linux tooling should resolve natively inside WSL unless cross-boundary integration is intentional.
- Source repositories should live under the Linux filesystem, such as ~/projects.

## External Services

- GitHub
- Microsoft Azure
- Container registries
