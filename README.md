# HashiCorp MCP Servers

This repository contains example configurations for running local MCP servers for HashiCorp Terraform and Vault.

## Prerequisites

- Docker and Docker Compose installed on your machine.

## Quick start

1. Start the services from the repository root:

```powershell
docker compose up -d
```

2. Confirm the services are running (example):

```powershell
docker compose ps
# or check specific ports
Invoke-WebRequest http://localhost:8081/health -UseBasicParsing
```

## Files in this repository

- `docker-compose.yml` — service definitions used to start the example servers (edit ports/tokens as needed).