---
name: "windsurf-audit-logging"
description: |
  Configure AI interaction audit logging for compliance. Activate when users mention
  "audit logging", "compliance logging", "ai interaction logs", "security audit",
  or "activity tracking". Handles compliance and audit configuration. Use when analyzing or auditing windsurf audit logging. Trigger with phrases like "windsurf audit logging", "windsurf logging", "windsurf".
allowed-tools: "Read,Write,Edit,Bash(cmd:*)"
version: 1.0.0
license: MIT
author: "Jeremy Longshore <jeremy@intentsolutions.io>"
---

# Windsurf Audit Logging

Configure comprehensive audit logging for compliance and security requirements.

## Overview

This skill enables comprehensive audit logging for Windsurf Enterprise deployments. It covers AI interaction logging, file access tracking, authentication events, and configuration changes. Proper audit logging ensures compliance with SOC 2, ISO 27001, HIPAA, and other security frameworks while providing forensic capabilities for security investigations.

## Prerequisites

- Windsurf Enterprise subscription
- Organization administrator access
- Compliance requirements documented
- Log storage infrastructure
- SIEM integration (optional but recommended)

## Directory Structure

```
organization-config/
    .windsurf-enterprise/
        audit/
            config/
                logging-config.json      # Audit logging settings
                    # Log levels and categories
                    # Retention periods
                    # Export destinations

                events-config.json       # Event tracking rules
                    # Tracked event types
                    # Sampling rates
                    # Priority levels

            schemas/
                ai-interaction.schema.json   # AI interaction log schema
                    # Request details
                    # Response metadata
                    # Token usage

                file-access.schema.json      # File access log schema
                    # File paths
                    # Action types
                    # User attribution

                auth-event.schema.json       # Authentication log schema
                    # Login events
                    # Session management
                    # Permission changes

            exports/
                siem-integration.json        # SIEM integration config
                    # Connector settings
                    # Field mappings
                    # Filter rules

                s3-export.json               # S3 export configuration
                    # Bucket settings
                    # Encryption options
                    # Lifecycle rules

            reports/
                templates/
                    daily-summary.json       # Daily activity report
                    weekly-audit.json        # Weekly audit report
                    compliance-report.json   # Compliance status report
```

## Audit Features

### Event Categories
- AI interactions (prompts, completions)
- File access and modifications
- Authentication events
- Configuration changes

### Compliance Support
- SOC 2 Type II
- ISO 27001
- HIPAA (with BAA)
- GDPR

## Instructions

1. **Enable Audit Logging**
   - Configure event categories to capture
   - Set log levels (info, warn, error)
   - Define retention periods

2. **Configure Event Types**
   - Enable AI interaction logging
   - Set up file access tracking
   - Configure authentication logging

3. **Set Up Integrations**
   - Connect to SIEM if available
   - Configure S3 or cloud storage export
   - Set up real-time alerting

4. **Create Reports**
   - Schedule daily summaries
   - Configure weekly audit reports
   - Set up compliance reporting

5. **Monitor and Alert**
   - Define anomaly detection rules
   - Set up alert thresholds
   - Configure notification channels

## Output

- Configured audit log streams
- SIEM integration
- Automated reports
- Alert configurations

## Error Handling

| Error | Cause | Solution |
|-------|-------|----------|
| Log export failed | Storage permission issue | Check IAM permissions, bucket policy |
| Missing events | Category not enabled | Enable required event categories |
| SIEM connection failed | Network or auth issue | Verify connector settings, credentials |
| Retention violation | Logs deleted too early | Update retention policy, restore if possible |
| Report generation failed | Template error | Validate report template syntax |

## Examples

**Example: Enable Full Audit Logging**
Request: "Set up comprehensive audit logging for SOC 2 compliance"
Result: All event categories enabled, 1-year retention, SIEM integration

**Example: Configure SIEM Integration**
Request: "Connect Windsurf audit logs to Splunk"
Result: Splunk connector configured, field mappings, real-time forwarding

**Example: Create Compliance Report**
Request: "Generate weekly compliance report for security team"
Result: Scheduled report with auth events, access patterns, anomalies

## Resources

- [Windsurf Audit Logging Guide](https://docs.windsurf.ai/admin/audit)
- [SOC 2 Compliance Documentation](https://docs.windsurf.ai/compliance/soc2)
- [SIEM Integration Guide](https://docs.windsurf.ai/admin/siem)

## Success Criteria

- All AI interactions logged
- Timestamps and user attribution
- SOC 2 and ISO 27001 compliance satisfied
