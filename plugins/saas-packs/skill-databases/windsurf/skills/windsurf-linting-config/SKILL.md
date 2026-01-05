---
name: "windsurf-linting-config"
description: |
  Configure and enforce code quality with AI-assisted linting. Activate when users mention
  "configure linting", "eslint setup", "code quality rules", "linting configuration",
  or "code standards". Handles linting tool configuration. Use when configuring systems or services. Trigger with phrases like "windsurf linting config", "windsurf config", "windsurf".
allowed-tools: "Read,Write,Edit,Bash(cmd:*)"
version: 1.0.0
license: MIT
author: "Jeremy Longshore <jeremy@intentsolutions.io>"
---

# Windsurf Linting Configuration

Configure and enforce code quality with AI-assisted linting.

## Overview

This skill enables comprehensive linting configuration within Windsurf. Cascade assists with ESLint, Prettier, Stylelint, and other linting tool setup, helping resolve configuration conflicts, suggesting rules based on project patterns, and automating code quality enforcement. Proper linting configuration catches errors early and maintains consistent code style.

## Prerequisites

- Windsurf IDE with Cascade enabled
- Node.js for JavaScript/TypeScript projects
- Package manager (npm, yarn, pnpm)
- Understanding of code style preferences
- Team agreement on quality standards

## Directory Structure

```
project-root/
    .eslintrc.js                     # ESLint configuration
        # Rule definitions
        # Plugin configuration
        # Environment settings
        # Override patterns

    .eslintignore                    # ESLint exclusions
        # Build directories
        # Generated files
        # Third-party code

    .prettierrc                      # Prettier configuration
        # Format rules
        # Parser options
        # Plugin settings

    .prettierignore                  # Prettier exclusions
        # Minified files
        # Vendor code
        # Lock files

    .stylelintrc.js                  # CSS/SCSS linting
        # Style rules
        # Property ordering
        # Selector patterns

    .windsurf/
        linting/
            profiles/
                strict.eslintrc.js       # Strict rule set
                    # Maximum enforcement
                    # No warnings allowed
                    # All best practices

                relaxed.eslintrc.js      # Relaxed rule set
                    # Essential rules only
                    # Warning level for style
                    # Flexible formatting

            custom-rules/
                project-rules.js         # Project-specific rules
                    # Custom patterns
                    # Domain-specific checks
                    # Team conventions

            auto-fix-config.json         # Auto-fix preferences
                # Rules to auto-fix
                # Confirmation requirements
                # Exclusion patterns
```

## Linting Features

### ESLint Integration
- Real-time error highlighting
- Auto-fix on save
- Custom rule support
- Plugin ecosystem

### AI Enhancement
- Rule suggestion based on code patterns
- Conflict resolution
- Performance optimization
- Migration assistance

## Instructions

1. **Choose Base Configuration**
   - Select framework preset (Airbnb, Standard, etc.)
   - Enable relevant plugins
   - Set environment targets

2. **Configure Rules**
   - Adjust severity levels (error, warn, off)
   - Add project-specific rules
   - Configure exception patterns

3. **Set Up Prettier Integration**
   - Install eslint-config-prettier
   - Configure format rules
   - Set up format on save

4. **Add Pre-Commit Hooks**
   - Configure lint-staged
   - Set up Husky hooks
   - Add commit blocking for errors

5. **Integrate with CI**
   - Add linting to CI pipeline
   - Configure failure thresholds
   - Set up reporting

## Output

- Configured .eslintrc.js
- Prettier configuration
- Pre-commit hooks
- CI integration

## Error Handling

| Error | Cause | Solution |
|-------|-------|----------|
| Rule conflict | ESLint/Prettier clash | Use eslint-config-prettier |
| Parser error | Wrong parser configured | Set parser for file type |
| Plugin not found | Missing dependency | Install plugin package |
| Performance issue | Too many rules/files | Add .eslintignore entries |
| Auto-fix breaks code | Aggressive auto-fix | Disable auto-fix for rule |

## Examples

**Example: Set Up TypeScript Linting**
Request: "Configure ESLint for TypeScript with React"
Result: ESLint config with @typescript-eslint, React hooks rules, Prettier integration

**Example: Resolve Linting Conflicts**
Request: "Fix conflicts between ESLint and Prettier"
Result: eslint-config-prettier installed, conflicting rules disabled

**Example: Create Strict Profile**
Request: "Set up strict linting for production code"
Result: Strict profile with all errors, no warnings, max enforcement

## Resources

- [Windsurf Linting Guide](https://docs.windsurf.ai/features/linting)
- [ESLint Documentation](https://eslint.org/docs/latest/)
- [Prettier Integration](https://prettier.io/docs/en/integrating-with-linters.html)

## Success Criteria

- Zero false positives
- Auto-fix capability for most issues
- 90% reduction in style-related review comments
