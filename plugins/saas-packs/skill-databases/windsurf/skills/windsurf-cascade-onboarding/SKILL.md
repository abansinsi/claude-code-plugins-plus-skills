---
name: "windsurf-cascade-onboarding"
description: |
  Configure Cascade AI agent for new team projects. Activate when users mention
  "setup cascade", "configure windsurf ai", "initialize cascade agent", "new windsurf project",
  or "onboard team to windsurf". Handles agent configuration, context settings, and team defaults. Use when working with windsurf cascade onboarding functionality. Trigger with phrases like "windsurf cascade onboarding", "windsurf onboarding", "windsurf".
allowed-tools: "Read,Write,Edit,Bash(cmd:*),Grep,Glob"
version: 1.0.0
license: MIT
author: "Jeremy Longshore <jeremy@intentsolutions.io>"
---

# Windsurf Cascade Onboarding

Configure Cascade AI agent for optimal team productivity from day one.

## Overview

This skill enables rapid onboarding of projects to Windsurf with optimized Cascade AI configuration. It covers creating .windsurfrules, setting up project context, configuring team defaults, and establishing best practices for AI-assisted development. Teams can achieve maximum Cascade productivity within the first week of adoption.

## Prerequisites

- Windsurf IDE installed for all team members
- Active Cascade AI subscription
- Project documentation (architecture, conventions)
- Team lead or admin access for configuration
- Understanding of project structure and patterns

## Directory Structure

```
project-root/
    .windsurfrules           # Project-specific AI rules and context
        # YAML configuration defining Cascade behavior patterns
        # Includes code style preferences, framework conventions
        # Custom instructions for project-specific patterns

    .windsurf/
        cascade-config.json  # Cascade agent settings
            # Model preferences and temperature settings
            # Context window configuration
            # Response format preferences

        context/
            project-context.md   # High-level project description
                # Architecture overview for AI understanding
                # Key dependencies and their purposes
                # Team conventions and coding standards

            patterns.md          # Common patterns in codebase
                # Design patterns used in project
                # API conventions and naming schemes
                # Error handling approaches

        snippets/
            README.md            # Snippet library documentation
                # How to add new snippets
                # Snippet naming conventions

            component.snippet    # Reusable code templates
                # Framework-specific component templates
                # Common boilerplate patterns

    docs/
        windsurf-guide.md    # Team Windsurf usage guide
            # Best practices for Cascade interactions
            # Common prompts and their use cases
            # Troubleshooting common issues
```

## Instructions

1. **Initialize Windsurf Rules**
   - Create `.windsurfrules` file in project root
   - Define project language and framework preferences
   - Set up code style and naming conventions

2. **Configure Cascade Context**
   - Write project architecture documentation
   - Document key patterns and conventions
   - Include dependency documentation and purposes

3. **Set Up Team Defaults**
   - Configure shared snippets library
   - Establish prompt templates for common tasks
   - Document best practices for Cascade usage

4. **Train Team Members**
   - Share windsurf-guide.md with team
   - Conduct onboarding sessions
   - Establish feedback channels for improvements

5. **Iterate Based on Feedback**
   - Collect team feedback weekly
   - Refine context and rules
   - Update documentation continuously

## Output

- Configured .windsurfrules file
- Project context documentation
- Team snippet library
- Onboarding guide for new members

## Error Handling

| Error | Cause | Solution |
|-------|-------|----------|
| Cascade not understanding project | Missing context | Add more project documentation to context/ |
| Inconsistent code style | Rules not specific enough | Expand .windsurfrules with specific patterns |
| Slow response times | Too much context loaded | Prioritize essential context, remove redundant |
| Team confusion | Inadequate training | Update guide, conduct additional training |
| Context not persisting | Configuration issue | Check cascade-config.json settings |

## Examples

**Example: Set Up React Project**
Request: "Configure Cascade for our React TypeScript project"
Result: .windsurfrules with React patterns, component templates, and styling conventions

**Example: Configure Python ML Project**
Request: "Onboard our machine learning project to Windsurf"
Result: Context with ML patterns, Jupyter integration, and data science conventions

**Example: Enterprise Backend Setup**
Request: "Set up Windsurf for our Java Spring Boot microservices"
Result: Service patterns, API conventions, and enterprise architecture context

## Resources

- [Windsurf Onboarding Guide](https://docs.windsurf.ai/getting-started/onboarding)
- [Writing Effective .windsurfrules](https://docs.windsurf.ai/features/windsurfrules)
- [Team Best Practices](https://docs.windsurf.ai/guides/team-best-practices)

## Success Criteria

- Cascade responds within 2 seconds to prompts
- Context maintained across 50+ file edits
- Team productivity increases 40% in first week
