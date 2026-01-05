---
name: "windsurf-cicd-github-actions"
description: |
  Generate and maintain GitHub Actions with Cascade assistance. Activate when users mention
  "github actions", "ci/cd pipeline", "workflow automation", "continuous integration",
  or "deployment pipeline". Handles CI/CD configuration with AI assistance. Use when working with windsurf cicd github actions functionality. Trigger with phrases like "windsurf cicd github actions", "windsurf actions", "windsurf".
allowed-tools: "Read,Write,Edit,Bash(cmd:*),Grep"
version: 1.0.0
license: MIT
author: "Jeremy Longshore <jeremy@intentsolutions.io>"
---

# Windsurf CI/CD GitHub Actions

Generate and maintain GitHub Actions workflows with Cascade AI assistance.

## Overview

This skill enables AI-assisted CI/CD workflow creation within Windsurf. Cascade can generate GitHub Actions workflows from project requirements, optimize existing pipelines, debug workflow failures, and implement security best practices. It understands common CI/CD patterns and can create workflows for testing, building, and deploying applications.

## Prerequisites

- Windsurf IDE with Cascade enabled
- GitHub repository with write access
- Understanding of CI/CD concepts
- GitHub Actions enabled on repository
- Deployment targets configured (if applicable)

## Directory Structure

```
project-root/
    .github/
        workflows/
            ci.yml                   # Continuous integration workflow
                # Test execution on push/PR
                # Linting and type checking
                # Build verification

            cd.yml                   # Continuous deployment workflow
                # Production deployment steps
                # Environment configuration
                # Rollback procedures

            pr-checks.yml            # Pull request validation
                # Code review automation
                # Preview deployments
                # Status checks

            release.yml              # Release automation
                # Version bumping
                # Changelog generation
                # Asset publishing

        actions/
            custom-action/
                action.yml           # Reusable action definition
                    # Input parameters
                    # Output definitions
                    # Execution steps

        CODEOWNERS                   # Code ownership rules
            # Team responsibilities
            # Review requirements

    .windsurf/
        cicd/
            workflow-templates/
                standard-ci.yml      # Standard CI template
                    # Common job definitions
                    # Matrix configurations
                    # Caching strategies

            secrets-reference.md     # Required secrets documentation
                # Secret names and purposes
                # Rotation schedules
                # Access requirements
```

## Workflow Patterns

### Standard CI
- Checkout and cache setup
- Dependency installation
- Linting and type checking
- Test execution with coverage
- Build verification

### Deployment
- Environment-based triggers
- Approval gates
- Blue-green deployment
- Health checks

## Instructions

1. **Analyze Requirements**
   - Identify build and test steps
   - Map deployment targets
   - Document secret requirements

2. **Generate Workflows**
   - Use Cascade for initial generation
   - Customize triggers and conditions
   - Add environment variables

3. **Configure Secrets**
   - Set up repository secrets
   - Document secret purposes
   - Plan rotation schedule

4. **Test Workflows**
   - Run workflows on test branches
   - Debug failures with Cascade
   - Optimize for speed

5. **Deploy and Monitor**
   - Enable on main branch
   - Set up failure notifications
   - Monitor execution times

## Output

- GitHub Actions workflow files
- Reusable action definitions
- Secrets documentation
- CODEOWNERS configuration

## Error Handling

| Error | Cause | Solution |
|-------|-------|----------|
| Workflow syntax error | Invalid YAML | Validate with actionlint or yamllint |
| Secret not found | Missing repository secret | Add secret in repository settings |
| Permission denied | Insufficient GITHUB_TOKEN | Add required permissions to workflow |
| Cache miss | Cache key mismatch | Update cache key pattern |
| Deploy failed | Environment misconfiguration | Check environment secrets and settings |

## Examples

**Example: Generate CI Workflow**
Request: "Create CI workflow for Node.js with TypeScript"
Result: Workflow with checkout, cache, install, lint, test, build steps

**Example: Add Deployment Stage**
Request: "Add staging and production deployment to our pipeline"
Result: CD workflow with environment-specific jobs, approval gates

**Example: Debug Workflow Failure**
Request: "Our CI workflow is failing at the test step"
Result: Analysis of failure, fix for environment variable or dependency issue

## Resources

- [Windsurf CI/CD Guide](https://docs.windsurf.ai/features/cicd)
- [GitHub Actions Documentation](https://docs.github.com/en/actions)
- [Workflow Syntax Reference](https://docs.github.com/en/actions/reference/workflow-syntax-for-github-actions)

## Success Criteria

- Workflows pass validation
- Successful execution on first commit
- Pipeline setup in hours vs days
