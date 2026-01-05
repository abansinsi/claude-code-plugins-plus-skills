---
name: "windsurf-usage-analytics"
description: |
  Analyze team AI usage patterns and productivity metrics. Activate when users mention
  "usage analytics", "ai metrics", "productivity tracking", "usage reports",
  or "roi analysis". Handles analytics and reporting configuration. Use when working with windsurf usage analytics functionality. Trigger with phrases like "windsurf usage analytics", "windsurf analytics", "windsurf".
allowed-tools: Read,Grep,Glob
version: 1.0.0
license: MIT
author: "Jeremy Longshore <jeremy@intentsolutions.io>"
---

# Windsurf Usage Analytics

Analyze team AI usage patterns for productivity insights and ROI measurement.

## Overview

This skill enables comprehensive usage analytics for Windsurf deployments. It tracks AI feature adoption, measures productivity improvements, calculates ROI, and identifies optimization opportunities. Analytics data helps justify AI investment, identify training needs, and optimize license allocation based on actual usage patterns.

## Prerequisites

- Windsurf Enterprise subscription
- Organization administrator access
- Analytics collection enabled
- Dashboard access configured
- Understanding of key metrics

## Directory Structure

```
organization-config/
    .windsurf-enterprise/
        analytics/
            config/
                tracking-config.json         # Analytics configuration
                    # Tracked metrics
                    # Sampling rates
                    # Privacy filters

                dashboard-config.json        # Dashboard settings
                    # Widget definitions
                    # Refresh intervals
                    # Access controls

            metrics/
                productivity/
                    code-velocity.json       # Code output metrics
                        # Lines written/modified
                        # Commits per day
                        # PR cycle time

                    ai-acceptance.json       # AI acceptance rates
                        # Completion acceptance
                        # Suggestion quality
                        # Time saved

                    time-savings.json        # Time efficiency
                        # Task completion time
                        # Debugging duration
                        # Code review time

                adoption/
                    feature-usage.json       # Feature adoption
                        # Cascade usage frequency
                        # Flow utilization
                        # Extension adoption

                    user-engagement.json     # User engagement
                        # Daily active users
                        # Session duration
                        # Feature discovery

            reports/
                templates/
                    executive-summary.json       # Executive dashboard
                    team-performance.json        # Team metrics
                    roi-calculation.json         # ROI analysis

                scheduled/
                    weekly-report.json           # Weekly summary
                    monthly-analytics.json       # Monthly trends
                    quarterly-review.json        # Quarterly analysis
```

## Analytics Features

### Productivity Metrics
- Code velocity measurements
- AI suggestion acceptance rates
- Time savings calculations
- Quality improvements

### Adoption Tracking
- Feature utilization
- User engagement
- Learning progress
- Best practice adoption

## Instructions

1. **Enable Analytics**
   - Configure tracking settings
   - Set privacy filters
   - Define key metrics

2. **Configure Dashboards**
   - Create executive dashboard
   - Build team performance views
   - Set up individual developer views

3. **Set Up Reporting**
   - Schedule weekly summaries
   - Configure monthly trend reports
   - Create ROI calculation reports

4. **Define Baselines**
   - Establish pre-Windsurf baselines
   - Set target improvements
   - Configure comparison periods

5. **Monitor and Optimize**
   - Review adoption trends
   - Identify training opportunities
   - Optimize license allocation

## Output

- Analytics dashboards
- Productivity reports
- ROI calculations
- Adoption trend analysis

## Error Handling

| Error | Cause | Solution |
|-------|-------|----------|
| Metrics not collecting | Tracking disabled | Enable analytics in settings |
| Dashboard not loading | Permission issue | Check user access permissions |
| Report generation failed | Data missing | Verify data collection, check date range |
| ROI calculation invalid | Missing baseline | Establish pre-implementation baseline |
| Privacy concern flagged | PII in metrics | Update privacy filters, anonymize data |

## Examples

**Example: Configure Executive Dashboard**
Request: "Create dashboard showing AI productivity gains for leadership"
Result: Dashboard with time saved, acceptance rates, ROI summary

**Example: Calculate Team ROI**
Request: "Calculate ROI of Windsurf for our engineering team"
Result: Report showing hours saved, cost per developer, net productivity gain

**Example: Identify Training Needs**
Request: "Which features are underutilized by our team?"
Result: Adoption report showing low Flow usage, recommending training

## Resources

- [Windsurf Analytics Guide](https://docs.windsurf.ai/admin/analytics)
- [ROI Measurement Framework](https://docs.windsurf.ai/guides/roi)
- [Dashboard Configuration](https://docs.windsurf.ai/admin/dashboards)

## Success Criteria

- Accurate AI acceptance rate metrics
- Clear time savings data
- ROI data supports investment decisions
