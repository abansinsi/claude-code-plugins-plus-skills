---
name: "windsurf-extension-pack"
description: |
  Install and configure essential Windsurf extensions for productivity. Activate when users mention
  "install extensions", "setup windsurf plugins", "configure extensions", "extension recommendations",
  or "productivity extensions". Handles extension installation and configuration. Use when working with windsurf extension pack functionality. Trigger with phrases like "windsurf extension pack", "windsurf pack", "windsurf".
allowed-tools: "Read,Write,Bash(cmd:*)"
version: 1.0.0
license: MIT
author: "Jeremy Longshore <jeremy@intentsolutions.io>"
---

# Windsurf Extension Pack

Install and configure essential extensions for maximum Windsurf productivity.

## Overview

This skill enables rapid setup of Windsurf with essential extensions for productive development. It covers language support, linting, formatting, Git integration, and productivity tools. Create team-standard extension configurations that can be shared and automatically installed for consistent development environments across your organization.

## Prerequisites

- Windsurf IDE installed
- Internet connection for extension downloads
- Admin rights for system-wide extensions (optional)
- Understanding of team development requirements
- List of required language support needs

## Directory Structure

```
~/.windsurf/
    extensions/
        extension-manifest.json  # Installed extensions registry
            # Extension IDs and versions
            # Installation timestamps
            # Dependency mappings

        ms-python.python/        # Python language support
            # Interpreter configuration
            # Linting and formatting
            # Debugging support

        dbaeumer.vscode-eslint/  # JavaScript/TypeScript linting
            # ESLint configuration
            # Auto-fix settings
            # Rule customization

        esbenp.prettier-vscode/  # Code formatting
            # Formatter configuration
            # Language-specific settings
            # Format on save rules

project-root/
    .vscode/
        extensions.json          # Workspace extension recommendations
            # Required extensions list
            # Optional productivity tools
            # Development-specific extensions

        settings.json            # Extension-specific settings
            # Per-extension configuration
            # Workspace overrides
            # Feature toggles
```

## Recommended Extensions

### Essential
- **Python** - Full Python language support
- **ESLint** - JavaScript/TypeScript linting
- **Prettier** - Code formatting
- **GitLens** - Git integration enhancement

### Productivity
- **Error Lens** - Inline error display
- **Todo Tree** - Task tracking
- **Bracket Pair Colorizer** - Code readability
- **Path Intellisense** - File path completion

## Instructions

1. **Assess Requirements**
   - Identify languages used in project
   - List required linting and formatting tools
   - Document team-standard extensions

2. **Install Core Extensions**
   - Install language support extensions
   - Add linting and formatting tools
   - Configure Git enhancements

3. **Configure Extension Settings**
   - Set up formatters per language
   - Configure linting rules
   - Enable productivity features

4. **Create Team Configuration**
   - Build extensions.json with required extensions
   - Document extension purposes and settings
   - Set up automated installation scripts

5. **Document and Share**
   - Create onboarding documentation
   - Share configuration with team
   - Set up sync for updates

## Output

- Fully configured Windsurf environment
- extensions.json with team recommendations
- settings.json with extension configurations
- Documentation for extension usage

## Error Handling

| Error | Cause | Solution |
|-------|-------|----------|
| Extension install failed | Network or compatibility | Check internet, verify version compatibility |
| Extension conflict | Multiple extensions overlap | Disable conflicting extension, choose one |
| Settings not applied | JSON syntax error | Validate settings.json syntax |
| Extension not activating | Missing dependency | Install required dependencies |
| Performance issues | Too many extensions | Disable unused extensions, check resource usage |

## Examples

**Example: Set Up JavaScript Development Environment**
Request: "Install extensions for JavaScript development with React"
Result: ESLint, Prettier, React snippets, ES7+ React/Redux snippets installed and configured

**Example: Configure Python Data Science Environment**
Request: "Set up Windsurf for Python data science work"
Result: Python, Jupyter, Pylance, Python Docstring Generator installed

**Example: Create Team Extension Pack**
Request: "Create shareable extension configuration for backend team"
Result: extensions.json with backend-focused extensions, settings.json with team conventions

## Resources

- [Windsurf Extension Marketplace](https://marketplace.windsurf.ai)
- [Extension Development Guide](https://docs.windsurf.ai/extensions/development)
- [Team Extension Management](https://docs.windsurf.ai/admin/extensions)

## Success Criteria

- All extensions installed without conflicts
- Verified functionality for each extension
- Environment operational within 30 minutes
