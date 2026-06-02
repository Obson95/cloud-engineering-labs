# Lab 3 - Conditional Access and MFA
## Status: Could not complete - requires Entra ID P1 license

## What this lab covers:
- Creating a Conditional Access policy requiring MFA for all users
- Setting policy to Report-only mode before enforcing
- Excluding break-glass admin account from MFA policy

## Key concepts learned:
- Conditional Access requires Entra ID P1 minimum
- Always start with Report-only mode to see impact before enforcing
- Never include your emergency admin account in MFA policies - risk of lockout
- Policy logic: IF (condition) THEN (control)
  - Example: IF user outside network THEN require MFA
  - Example: IF user in Managers group THEN require compliant device

## Would implement in production by:
1. Entra admin center > Protection > Conditional Access > New policy
2. Name: "Require MFA for All Users"
3. Users: All users, EXCLUDE break-glass admin
4. Target resources: All cloud apps
5. Grant: Require multifactor authentication
6. Start in Report-only mode, monitor, then flip to On
