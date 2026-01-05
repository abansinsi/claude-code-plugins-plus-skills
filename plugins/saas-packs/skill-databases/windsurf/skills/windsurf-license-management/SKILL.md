---
name: "windsurf-license-management"
description: |
  Manage Windsurf licenses and seat allocation. Activate when users mention
  "license management", "seat allocation", "billing optimization", "user licenses",
  or "subscription management". Handles license administration. Use when working with windsurf license management functionality. Trigger with phrases like "windsurf license management", "windsurf management", "windsurf".
allowed-tools: Read,Write,Edit
version: 1.0.0
license: MIT
author: "Jeremy Longshore <jeremy@intentsolutions.io>"
---

# Windsurf License Management

Manage Windsurf licenses and optimize seat allocation for cost efficiency.

## Overview

This skill enables enterprise license management for Windsurf deployments. It covers seat allocation, usage tracking, cost optimization, and compliance reporting. Administrators can provision new users, reclaim inactive seats, analyze utilization patterns, and optimize subscription tiers based on actual usage data.

## Prerequisites

- Windsurf Enterprise subscription with admin access
- Organization administrator role
- Access to billing portal
- User directory integration (optional: SCIM, Azure AD, Okta)
- Understanding of organization structure and teams

## Directory Structure

```
organization-config/
    .windsurf-enterprise/
        licensing/
            config/
                license-config.json          # License configuration
                    # Subscription tier
                    # Seat count
                    # Billing cycle

                allocation-rules.json        # Seat allocation rules
                    # Priority criteria
                    # Auto-assignment rules
                    # Reclamation policies

            inventory/
                active-licenses.json         # Current allocations
                    # Assigned users
                    # Assignment dates
                    # Last activity

                available-seats.json         # Unassigned seats
                    # Available count
                    # Reserved seats
                    # Pending assignments

                historical/
                    YYYY-MM.json             # Monthly snapshots
                        # Usage trends
                        # Peak utilization
                        # Turnover data

            policies/
                usage-policy.json            # Usage requirements
                    # Minimum activity thresholds
                    # Grace periods
                    # Reclamation triggers

                provisioning-policy.json     # Provisioning rules
                    # Request workflow
                    # Approval requirements
                    # Onboarding timeline

            reports/
                utilization-report.json      # Usage efficiency
                    # Active vs allocated
                    # Cost per active user
                    # Optimization recommendations

                cost-analysis.json           # Cost breakdown
                    # Per-seat costs
                    # Feature utilization
                    # Comparison with alternatives
```

## License Features

### Seat Management
- Automated provisioning
- Usage-based reclamation
- Department allocation
- Cost center tracking

### Cost Optimization
- Utilization reporting
- Right-sizing recommendations
- Tier optimization
- Budget forecasting

## Instructions

1. **Inventory Current Licenses**
   - Export current seat allocations
   - Identify inactive users (no activity 30+ days)
   - Map licenses to cost centers or departments

2. **Set Allocation Policies**
   - Define eligibility criteria for seat assignment
   - Configure auto-provisioning rules
   - Set reclamation thresholds and grace periods

3. **Configure Usage Tracking**
   - Enable activity monitoring
   - Set up utilization reports
   - Configure alerts for low usage

4. **Optimize Subscription**
   - Review utilization reports
   - Reclaim unused seats
   - Right-size subscription tier

5. **Monitor and Report**
   - Schedule regular utilization reports
   - Track cost per active user
   - Report to stakeholders monthly

## Output

- License inventory with current allocations
- Utilization reports with recommendations
- Cost analysis with optimization opportunities
- Compliance reports for audits

## Error Handling

| Error | Cause | Solution |
|-------|-------|----------|
| Seat assignment failed | No available seats | Reclaim inactive seats or upgrade plan |
| User not found | SCIM sync issue | Verify directory integration |
| Reclamation blocked | User in grace period | Wait for grace period or override |
| Report generation failed | Missing data | Check activity tracking enabled |
| Billing discrepancy | Seat count mismatch | Reconcile with billing portal |

## Examples

**Example: Provision New Team**
Request: "Add 10 seats for the new mobile development team"
Result: Seats allocated, users provisioned, cost center assigned

**Example: Reclaim Inactive Seats**
Request: "Identify and reclaim seats inactive for more than 60 days"
Result: 15 seats identified, notifications sent, seats reclaimed after grace period

**Example: Generate Cost Report**
Request: "Create monthly license utilization report for finance"
Result: Report with active users, cost per user, and optimization recommendations

## Resources

- [Windsurf License Administration](https://docs.windsurf.ai/admin/licensing)
- [SCIM Integration Guide](https://docs.windsurf.ai/admin/scim)
- [Cost Optimization Best Practices](https://docs.windsurf.ai/admin/cost-optimization)

## Success Criteria

- Optimized utilization (no unused seats)
- Accurate billing alignment
- 20% reduction in software costs
