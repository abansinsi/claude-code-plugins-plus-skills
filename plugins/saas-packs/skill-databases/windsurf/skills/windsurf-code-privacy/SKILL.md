---
name: "windsurf-code-privacy"
description: |
  Configure code privacy and data retention policies. Activate when users mention
  "code privacy", "data retention", "privacy settings", "data governance",
  or "gdpr compliance". Handles privacy and data protection configuration. Use when working with windsurf code privacy functionality. Trigger with phrases like "windsurf code privacy", "windsurf privacy", "windsurf".
allowed-tools: Read,Write,Edit
version: 1.0.0
license: MIT
author: "Jeremy Longshore <jeremy@intentsolutions.io>"
---

# Windsurf Code Privacy

Configure code privacy and data retention policies for regulatory compliance.

## Overview

This skill enables comprehensive privacy configuration for Windsurf deployments. It covers data transmission controls, retention policies, regional compliance settings, and code exclusion patterns. Proper privacy configuration ensures your organization meets GDPR, CCPA, and other regulatory requirements while using AI-assisted development tools.

## Prerequisites

- Windsurf Enterprise subscription
- Organization administrator access
- Compliance requirements documented
- Legal/security team approval
- Understanding of data residency needs

## Directory Structure

```
organization-config/
    .windsurf-enterprise/
        privacy/
            config/
                privacy-settings.json        # Global privacy configuration
                    # Data transmission rules
                    # Local processing preferences
                    # Consent requirements

                retention-policy.json        # Data retention rules
                    # Retention periods by data type
                    # Deletion schedules
                    # Archive procedures

                consent-settings.json        # Consent management
                    # Required consents
                    # Opt-out options
                    # Preference storage

            exclusions/
                sensitive-patterns.json      # Sensitive content patterns
                    # Secret detection patterns
                    # PII patterns
                    # Proprietary code markers

                excluded-paths.json          # Excluded directories
                    # Paths never sent to AI
                    # Local-only processing
                    # Offline mode paths

            regional/
                eu-gdpr.json                 # GDPR compliance settings
                    # Data residency requirements
                    # Right to deletion
                    # Processing agreements

                us-ccpa.json                 # CCPA compliance settings
                    # Consumer rights
                    # Opt-out mechanisms
                    # Disclosure requirements

            documentation/
                privacy-policy.md            # User-facing policy
                    # Data collection practices
                    # Usage purposes
                    # User rights

                dpa-template.md              # Data processing agreement
                    # Legal requirements
                    # Subprocessor lists
                    # Security measures
```

## Privacy Features

### Data Protection
- End-to-end encryption
- Local processing options
- Selective code exclusion
- Audit trail maintenance

### Compliance
- GDPR compliance tools
- CCPA support
- Data residency options
- Right to deletion

## Instructions

1. **Assess Requirements**
   - Document regulatory requirements
   - Identify sensitive data types
   - Map data flows

2. **Configure Data Handling**
   - Set transmission policies
   - Define retention periods
   - Configure encryption settings

3. **Set Up Exclusions**
   - Define sensitive file patterns
   - Exclude specific directories
   - Mark proprietary code sections

4. **Enable Regional Compliance**
   - Configure GDPR settings for EU
   - Set up CCPA for US operations
   - Document data residency

5. **Document and Monitor**
   - Create privacy policy
   - Set up compliance monitoring
   - Enable audit logging

## Output

- Privacy configuration files
- Data exclusion patterns
- Retention policy documentation
- Compliance reports

## Error Handling

| Error | Cause | Solution |
|-------|-------|----------|
| Data transmission blocked | Exclusion pattern matched | Review pattern, whitelist if safe |
| Retention violation | Data not deleted on schedule | Check deletion job, manual cleanup |
| Consent missing | User not opted in | Prompt for consent, block until granted |
| Region mismatch | Data sent to wrong region | Update residency configuration |
| Audit gap | Logging disabled | Enable audit logging, investigate gap |

## Examples

**Example: Configure GDPR Compliance**
Request: "Set up Windsurf for GDPR compliance in EU operations"
Result: EU data residency, right to deletion, DPA templates configured

**Example: Exclude Sensitive Code**
Request: "Prevent our proprietary algorithms from being processed"
Result: Exclusion patterns for /proprietary/*, /algorithms/* directories

**Example: Configure Data Retention**
Request: "Set 30-day retention for AI interaction data"
Result: Retention policy with 30-day limit, automated deletion job

## Resources

- [Windsurf Privacy Guide](https://docs.windsurf.ai/admin/privacy)
- [GDPR Compliance Documentation](https://docs.windsurf.ai/compliance/gdpr)
- [Data Retention Best Practices](https://docs.windsurf.ai/guides/retention)

## Success Criteria

- Code never transmitted without consent
- Configurable retention active
- GDPR/CCPA requirements met
