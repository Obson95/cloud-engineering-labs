# Lab 4 - Enforce Tagging with Azure Policy

## What this lab covers:
- Assigning a built-in Azure Policy to require a CostCenter tag on all resources
- Testing policy enforcement by attempting to create resources without the tag
- Verifying policy denies non-compliant resources and allows compliant ones

## Policy details:
- Policy: "Require a tag on resources" (built-in)
- Policy Definition ID: 871b6d14-10aa-478d-b590-94f262ecfa99
- Tag required: CostCenter
- Scope: rg-devteam-lab resource group only
- Enforcement mode: Default (active)

## Key concepts learned:
- Built-in policies have definition IDs you can reference directly
- Policy assignments can take up to 30 minutes to propagate
- Policy scoped to a resource group only affects resources in that RG
- Resources created WITHOUT required tag = denied
- Resources created WITH required tag = allowed
- Tags are critical in enterprise environments for cost tracking

## Commands used:
- az policy assignment create = assign a policy to a scope
- az storage account create --tags CostCenter=Engineering = compliant resource
