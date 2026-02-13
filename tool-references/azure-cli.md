---
title: Azure CLI
order: 4
---

# Azure CLI Reference

Quick reference for common Azure CLI commands.

## Authentication

```bash
# Login
az login

# List subscriptions
az account list

# Set active subscription
az account set --subscription "My Subscription"

# Show current subscription
az account show
```

## Resource Groups

```bash
# List resource groups
az group list

# Create resource group
az group create --name mygroup --location eastus

# Delete resource group
az group delete --name mygroup
```

## App Service

```bash
# List web apps
az webapp list

# Create web app
az webapp create --name myapp --resource-group mygroup --plan myplan

# Deploy from local
az webapp deploy --name myapp --resource-group mygroup --src-path ./publish.zip

# View logs
az webapp log tail --name myapp --resource-group mygroup

# Restart
az webapp restart --name myapp --resource-group mygroup
```

## Azure SQL

```bash
# List servers
az sql server list

# Create database
az sql db create --name mydb --server myserver --resource-group mygroup

# Show connection string
az sql db show-connection-string --name mydb --server myserver --client ado.net
```

## Configuration

```bash
# Set app setting
az webapp config appsettings set --name myapp --resource-group mygroup --settings KEY=value

# List app settings
az webapp config appsettings list --name myapp --resource-group mygroup
```

---

See [DevOps: Azure](/devops/azure/overview) for detailed Azure guides.
