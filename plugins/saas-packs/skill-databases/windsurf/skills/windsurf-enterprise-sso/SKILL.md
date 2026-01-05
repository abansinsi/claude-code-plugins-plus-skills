---
name: "windsurf-enterprise-sso"
description: |
  Configure enterprise SSO integration for Windsurf. Activate when users mention
  "sso configuration", "single sign-on", "enterprise authentication", "saml setup",
  or "identity provider". Handles enterprise identity integration. Use when working with windsurf enterprise sso functionality. Trigger with phrases like "windsurf enterprise sso", "windsurf sso", "windsurf".
allowed-tools: "Read,Write,Edit,Bash(cmd:*)"
version: 1.0.0
license: MIT
author: "Jeremy Longshore <jeremy@intentsolutions.io>"
---

# Windsurf Enterprise SSO

Configure enterprise SSO integration for secure team authentication.

## Overview

This skill enables enterprise Single Sign-On (SSO) integration for Windsurf deployments. It supports SAML 2.0, OIDC/OAuth 2.0, and integration with major identity providers including Okta, Azure AD, and Google Workspace. Proper SSO configuration ensures secure authentication, simplified user management, and compliance with enterprise security requirements.

## Prerequisites

- Windsurf Enterprise subscription
- Organization administrator access
- Identity provider admin access
- Understanding of SAML/OIDC protocols
- Compliance requirements documented
- Certificate management capabilities

## Directory Structure

```
organization-config/
    .windsurf-enterprise/
        sso/
            config.json                  # SSO configuration
                # Identity provider settings
                # SAML/OIDC configuration
                # Attribute mappings

            providers/
                okta.json                # Okta configuration
                    # Application ID
                    # Domain settings
                    # Group mappings

                azure-ad.json            # Azure AD configuration
                    # Tenant ID
                    # Client configuration
                    # Role assignments

                google-workspace.json    # Google Workspace config
                    # Domain verification
                    # User provisioning
                    # Group sync settings

            certificates/
                README.md                # Certificate management guide
                    # Certificate requirements
                    # Rotation procedures
                    # Backup protocols

        policies/
            access-policy.json           # Access control rules
                # Role definitions
                # Permission sets
                # Group mappings

            session-policy.json          # Session management
                # Timeout settings
                # Concurrent session limits
                # Re-authentication triggers

        audit/
            auth-logs/
                README.md                # Audit log documentation
                    # Log format
                    # Retention policy
                    # Export procedures
```

## SSO Features

### Supported Providers
- SAML 2.0 identity providers
- OIDC/OAuth 2.0 providers
- Okta, Azure AD, Google Workspace
- Custom enterprise IdPs

### Security Features
- Multi-factor authentication support
- Session management
- Audit logging
- Just-in-time provisioning

## Instructions

1. **Prepare Identity Provider**
   - Create application registration in IdP
   - Configure redirect URIs
   - Set up attribute mappings (email, name, groups)

2. **Configure Windsurf SSO**
   - Enter IdP metadata or configuration
   - Map user attributes to Windsurf fields
   - Configure group sync for access control

3. **Set Up Certificates**
   - Generate or import signing certificates
   - Configure certificate rotation schedule
   - Set up backup certificates

4. **Configure Policies**
   - Define session timeout policies
   - Set MFA requirements
   - Configure access control rules

5. **Test and Enable**
   - Test with pilot user group
   - Verify MFA flow works correctly
   - Enable for entire organization

## Output

- Configured SSO integration
- User attribute mappings
- Group sync configuration
- Audit logging setup

## Error Handling

| Error | Cause | Solution |
|-------|-------|----------|
| SAML assertion failed | Certificate mismatch | Update certificates, verify metadata |
| User not provisioned | Missing attribute | Check attribute mapping configuration |
| MFA not triggering | Policy misconfiguration | Review MFA policy settings |
| Session timeout issues | Policy conflict | Align IdP and Windsurf session settings |
| Group sync failed | Permission issue | Verify IdP permissions for group access |

## Examples

**Example: Configure Okta SSO**
Request: "Set up SSO with Okta for our organization"
Result: SAML 2.0 integration with Okta, group sync, and MFA enabled

**Example: Azure AD Integration**
Request: "Integrate Windsurf with Azure AD for authentication"
Result: OIDC configuration with Azure AD, role-based access control

**Example: Enable MFA Requirement**
Request: "Require MFA for all Windsurf users"
Result: Policy configured to enforce MFA at every authentication

## Resources

- [Windsurf SSO Guide](https://docs.windsurf.ai/admin/sso)
- [SAML 2.0 Configuration](https://docs.windsurf.ai/admin/saml)
- [OIDC Configuration](https://docs.windsurf.ai/admin/oidc)

## Success Criteria

- SSO authentication functional
- MFA enabled and working
- Audit logging active
- Compliance requirements met
