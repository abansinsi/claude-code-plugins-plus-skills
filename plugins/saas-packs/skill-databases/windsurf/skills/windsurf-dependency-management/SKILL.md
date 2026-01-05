---
name: "windsurf-dependency-management"
description: |
  Analyze and update dependencies with vulnerability scanning. Activate when users mention
  "update dependencies", "security audit", "npm audit", "vulnerability scan",
  or "dependency updates". Handles dependency analysis and updates. Use when working with windsurf dependency management functionality. Trigger with phrases like "windsurf dependency management", "windsurf management", "windsurf".
allowed-tools: "Read,Write,Edit,Bash(cmd:*),Grep"
version: 1.0.0
license: MIT
author: "Jeremy Longshore <jeremy@intentsolutions.io>"
---

# Windsurf Dependency Management

Analyze and update dependencies with AI-assisted vulnerability management.

## Overview

This skill enables comprehensive dependency management within Windsurf projects. Cascade analyzes your dependency tree, identifies security vulnerabilities, suggests safe updates, and helps plan migration paths for major version upgrades. It integrates with npm, yarn, pnpm, pip, and other package managers to provide actionable security insights and update recommendations.

## Prerequisites

- Windsurf IDE with Cascade enabled
- Package manager installed (npm, yarn, pnpm, pip)
- Project with package.json, requirements.txt, or equivalent
- Understanding of semantic versioning
- CI/CD pipeline for testing updates (recommended)

## Directory Structure

```
project-root/
    package.json                     # NPM dependencies
        # Direct dependencies
        # Dev dependencies
        # Peer dependencies
        # Version constraints

    package-lock.json                # Lock file
        # Exact versions
        # Integrity hashes
        # Dependency tree

    .npmrc                           # NPM configuration
        # Registry settings
        # Authentication
        # Scope mappings

    .windsurf/
        dependencies/
            audit-report.json            # Security audit results
                # Vulnerability details
                # Severity levels
                # Remediation steps

            update-plan.json             # Planned updates
                # Version changes
                # Breaking change notes
                # Migration requirements

            compatibility-matrix.json    # Version compatibility
                # Tested combinations
                # Known conflicts
                # Recommended versions

            policies/
                update-policy.json       # Update frequency rules
                    # Major version handling
                    # Security update urgency
                    # Testing requirements

                block-list.json          # Blocked packages
                    # License violations
                    # Known vulnerabilities
                    # Deprecated packages
```

## Dependency Features

### Security Scanning
- Automated vulnerability detection
- Severity classification
- Remediation guidance
- Continuous monitoring

### Update Management
- Semantic version analysis
- Breaking change detection
- Rollback preparation
- Changelog summarization

## Instructions

1. **Run Initial Audit**
   - Execute security scan (`npm audit` or equivalent)
   - Review vulnerability severity levels
   - Prioritize critical and high severity issues

2. **Analyze Update Paths**
   - Identify packages needing updates
   - Check for breaking changes in changelogs
   - Map dependency relationships

3. **Plan Updates**
   - Create update plan with safe updates first
   - Schedule breaking change updates separately
   - Prepare migration steps for major versions

4. **Apply and Verify**
   - Update packages incrementally
   - Run test suite after each batch
   - Monitor for runtime regressions

5. **Establish Monitoring**
   - Configure automated audit alerts
   - Set up dependency update notifications
   - Schedule regular audit reviews

## Output

- Security audit report with findings
- Update plan with prioritized changes
- Compatibility matrix for version combinations
- Migration guides for breaking changes

## Error Handling

| Error | Cause | Solution |
|-------|-------|----------|
| Peer dependency conflict | Incompatible versions | Use resolutions/overrides or update peer |
| Audit resolution unavailable | No patch available | Apply workaround or accept risk with justification |
| Build failure after update | Breaking change | Review changelog, apply migration steps |
| Lock file conflict | Concurrent updates | Regenerate lock file, coordinate team |
| Registry timeout | Network or rate limit | Retry with backoff, check network |

## Examples

**Example: Run Security Audit**
Request: "Scan dependencies for security vulnerabilities"
Result: Audit report with 3 critical, 5 high severity issues and remediation steps

**Example: Plan Safe Updates**
Request: "Identify dependencies that can be safely updated"
Result: List of 15 packages with minor/patch updates and no breaking changes

**Example: Major Version Migration**
Request: "Help migrate from React 17 to React 18"
Result: Migration plan with breaking changes, code modifications needed, and testing checklist

## Resources

- [Windsurf Dependency Management](https://docs.windsurf.ai/features/dependencies)
- [npm Audit Documentation](https://docs.npmjs.com/cli/audit)
- [Semantic Versioning Spec](https://semver.org/)

## Success Criteria

- Zero high/critical CVEs
- Updates applied without breaking changes
- Minimal developer intervention required
