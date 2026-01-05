---
name: "windsurf-workspace-setup"
description: |
  Initialize Windsurf workspace with project-specific AI rules. Activate when users mention
  "create windsurfrules", "setup workspace", "configure project ai", "initialize windsurf workspace",
  or "migrate to windsurf". Handles workspace configuration and team standardization. Use when working with windsurf workspace setup functionality. Trigger with phrases like "windsurf workspace setup", "windsurf setup", "windsurf".
allowed-tools: "Read,Write,Edit,Bash(cmd:*)"
version: 1.0.0
license: MIT
author: "Jeremy Longshore <jeremy@intentsolutions.io>"
---

# Windsurf Workspace Setup

Initialize and configure Windsurf workspace for consistent AI-assisted development.

## Overview

This skill enables rapid workspace setup for Windsurf projects. It covers creating .windsurfrules for AI behavior, configuring editor settings, establishing team conventions, and setting up multi-root workspaces. Proper workspace setup ensures consistent AI assistance across all team members and projects.

## Prerequisites

- Windsurf IDE installed
- Project repository cloned
- Understanding of project architecture
- Team conventions documented
- Admin access for team-wide settings (optional)

## Directory Structure

```
project-root/
    .windsurfrules               # Primary AI configuration file
        # YAML-formatted rules for Cascade behavior
        # Project-specific coding conventions
        # Framework and library preferences
        # Security and compliance requirements

    .vscode/
        settings.json            # Editor settings (Windsurf compatible)
            # Windsurf-specific configuration overrides
            # Theme and UI preferences
            # Extension settings

        extensions.json          # Recommended extensions list
            # Essential Windsurf extensions
            # Language-specific tools
            # Team productivity extensions

    .editorconfig                # Cross-editor consistency
        # Indentation and whitespace rules
        # Line ending configuration
        # File encoding standards

    .gitattributes               # Git handling rules
        # Line ending normalization
        # Binary file handling
        # Merge strategy definitions

    workspace.code-workspace     # Multi-root workspace config
        # Folder definitions for monorepos
        # Shared settings across projects
        # Task and launch configurations
```

## Instructions

1. **Create .windsurfrules**
   - Define project language and framework
   - Set coding style preferences
   - Configure AI behavior guidelines

2. **Configure Editor Settings**
   - Set up formatter and linter settings
   - Configure language-specific options
   - Enable productivity features

3. **Set Up Extensions**
   - Install required extensions
   - Document recommended extensions
   - Configure extension settings

4. **Configure Cross-Editor Consistency**
   - Create .editorconfig file
   - Set up .gitattributes
   - Document encoding standards

5. **Establish Team Standards**
   - Document configuration decisions
   - Create onboarding checklist
   - Set up validation scripts

## Output

- Configured .windsurfrules file
- Editor settings.json
- Extension recommendations
- Cross-editor configuration files
- Workspace configuration for monorepos

## Error Handling

| Error | Cause | Solution |
|-------|-------|----------|
| YAML syntax error | Invalid .windsurfrules | Validate YAML syntax, check indentation |
| Extension conflict | Incompatible extensions | Disable conflicting extension |
| Settings not applied | JSON syntax error | Validate settings.json syntax |
| Inconsistent formatting | Missing .editorconfig | Create .editorconfig with team rules |
| Workspace not loading | Invalid .code-workspace | Check JSON syntax and folder paths |

## Examples

**Example: Set Up TypeScript Project**
Request: "Initialize Windsurf workspace for TypeScript Node.js project"
Result: .windsurfrules with TypeScript patterns, settings.json with ESLint/Prettier config

**Example: Configure Monorepo Workspace**
Request: "Set up multi-root workspace for our monorepo"
Result: workspace.code-workspace with folder mappings and shared settings

**Example: Migrate from VS Code**
Request: "Migrate our VS Code setup to Windsurf"
Result: Settings copied, extensions mapped, .windsurfrules created from conventions

## Resources

- [Windsurf Workspace Guide](https://docs.windsurf.ai/features/workspace)
- [.windsurfrules Reference](https://docs.windsurf.ai/reference/windsurfrules)
- [Multi-Root Workspaces](https://docs.windsurf.ai/features/multi-root)

## Success Criteria

- Valid YAML syntax in .windsurfrules
- Consistent AI behavior across team members
- 60% reduction in onboarding time
