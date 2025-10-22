# HashiCorp MCP Servers

This repository contains example configurations for running local MCP servers for HashiCorp Terraform and Vault.

## Prerequisites

- You have Docker and Docker Compose installed on your machine.
- `docker-compose.yml` in this repo brings up at least two services:
	- a Terraform MCP-style control plane (example: exposes a UI/API)
	- a Vault server (default Vault port 8200)
- This README uses PowerShell (`pwsh`) snippets because you're on Windows.

If your setup uses different ports or service names, replace `localhost:8200` and other placeholders accordingly.

## Quick start

1. Start the services from the repository root:

```powershell
docker-compose up -d
```

2. Confirm the services are running (example):

```powershell
docker-compose ps
# or check specific ports
Invoke-WebRequest http://localhost:8200 -UseBasicParsing
```

## Files in this repository

- `docker-compose.yml` — service definitions used to start the example servers (edit ports/tokens as needed).