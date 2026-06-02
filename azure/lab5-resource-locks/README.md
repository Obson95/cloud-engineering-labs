# Lab 5 - Resource Locks

## What this lab covers:
- Applying a CanNotDelete lock to a resource group
- Testing that deletion is blocked while lock is active

## Lock types:
- CanNotDelete = read and modify allowed, delete blocked
- ReadOnly = read only, no modify or delete

## Key concepts learned:
- Locks protect critical resources from accidental deletion
- Even Owner role cannot delete a locked resource
- Must remove lock before deletion is possible
- Locks are inherited by all resources inside the locked scope

## Commands used:
- az lock create --lock-type CanNotDelete
- az lock delete --name --resource-group
