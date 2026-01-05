---
name: "windsurf-team-settings"
description: |
  Manage team-wide Windsurf settings and AI policies. Activate when users mention
  "team settings", "organization config", "team policies", "shared settings",
  or "team standardization". Handles team configuration management. Use when working with windsurf team settings functionality. Trigger with phrases like "windsurf team settings", "windsurf settings", "windsurf".
allowed-tools: Read,Write,Edit
version: 1.0.0
license: MIT
author: "Jeremy Longshore <jeremy@intentsolutions.io>"
---

# Windsurf Team Settings

Manage team-wide settings and AI policies for consistent developer experience.

## Overview

This skill enables centralized management of Windsurf settings across teams and organizations. It covers editor preferences, AI behavior policies, tool approvals, and compliance requirements. Administrators can define organization-wide defaults with team-specific overrides, ensuring consistency while accommodating specialized team needs.

## Prerequisites

- Windsurf Enterprise subscription
- Organization administrator role
- Understanding of team structure and needs
- Compliance requirements documentation
- Team feedback on desired settings

## Directory Structure

```
organization-config/
    .windsurf-team/
        settings/
            global-settings.json         # Organization-wide defaults
                # Editor preferences
                # AI behavior settings
                # Feature toggles

            team-overrides/
                engineering.json         # Engineering team settings
                    # Development preferences
                    # Tool integrations
                    # Language configurations

                security.json            # Security team settings
                    # Restricted features
                    # Audit requirements
                    # Compliance settings

        policies/
            ai-usage-policy.json         # AI feature policies
                # Allowed AI features
                # Data handling rules
                # Usage restrictions

            code-sharing-policy.json     # Code sharing rules
                # Snippet sharing permissions
                # External tool integrations
                # Repository access

            tool-approval.json           # Approved tool list
                # Approved extensions
                # Blocked extensions
                # Pending review

        templates/
            new-member-settings.json     # Onboarding defaults
                # Initial configuration
                # Required extensions
                # Training resources

            project-settings.json        # Project template
                # Standard configurations
                # Recommended structure
                # Quality requirements
```

## Team Features

### Centralized Management
- Organization-wide defaults
- Team-specific overrides
- Role-based settings
- Version-controlled configuration

### Policy Enforcement
- AI usage policies
- Data handling rules
- Tool approval workflows
- Compliance requirements

## Instructions

1. **Define Organization Defaults**
   - Document baseline configuration requirements
   - Enable required features organization-wide
   - Disable restricted features globally

2. **Create Team Overrides**
   - Identify teams with specialized needs
   - Document exceptions and justifications
   - Create team-specific override files

3. **Set Up Policies**
   - Define AI usage policies
   - Configure code sharing rules
   - Establish tool approval workflow

4. **Deploy Settings**
   - Push settings to all team members
   - Configure automatic sync
   - Set up change notifications

5. **Monitor and Iterate**
   - Track policy compliance
   - Gather team feedback
   - Update settings based on needs

## Output

- Organization-wide settings configuration
- Team-specific override files
- Policy documentation
- Compliance reports

## Error Handling

| Error | Cause | Solution |
|-------|-------|----------|
| Settings not syncing | Network or permission issue | Check connectivity, verify user permissions |
| Override conflict | Conflicting team settings | Review and prioritize conflicting settings |
| Policy violation detected | User action against policy | Review policy, provide guidance or exception |
| Extension blocked | Not on approved list | Submit for approval or add to approved list |
| Settings reset | User override removed | Re-enable user overrides or update global |

## Examples

**Example: Configure Organization Defaults**
Request: "Set up default Windsurf settings for all developers"
Result: Global settings with formatting, linting, and AI behavior configured

**Example: Create Security Team Override**
Request: "Security team needs stricter AI policies than default"
Result: Team override with enhanced audit logging and restricted AI features

**Example: Enforce Extension Policy**
Request: "Only allow approved extensions organization-wide"
Result: Tool approval policy with whitelist and request workflow

## Resources

- [Windsurf Team Administration](https://docs.windsurf.ai/admin/team-settings)
- [Policy Configuration Guide](https://docs.windsurf.ai/admin/policies)
- [Settings Sync Documentation](https://docs.windsurf.ai/features/settings-sync)

## Success Criteria

- Settings synchronized within 5 minutes
- Consistent experience across team
- 40% reduction in support tickets
