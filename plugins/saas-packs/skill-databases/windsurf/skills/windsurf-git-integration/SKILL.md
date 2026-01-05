---
name: "windsurf-git-integration"
description: |
  Configure Git integration with Cascade AI assistance. Activate when users mention
  "git setup", "version control", "commit messages", "branch management",
  or "source control". Handles Git configuration and AI-assisted workflows. Use when working with windsurf git integration functionality. Trigger with phrases like "windsurf git integration", "windsurf integration", "windsurf".
allowed-tools: "Read,Write,Edit,Bash(cmd:*)"
version: 1.0.0
license: MIT
author: "Jeremy Longshore <jeremy@intentsolutions.io>"
---

# Windsurf Git Integration

Configure Git workflows enhanced by Cascade AI assistance.

## Overview

This skill enables AI-assisted Git workflows within Windsurf. Cascade can generate commit messages from staged changes, suggest branch names, assist with merge conflict resolution, and automate common Git operations. It integrates with hooks for validation and provides intelligent suggestions that follow your team's conventions.

## Prerequisites

- Git installed and configured
- Windsurf IDE with Cascade enabled
- Git repository initialized
- SSH keys or HTTPS credentials configured
- Understanding of team Git workflow (GitFlow, trunk-based, etc.)

## Directory Structure

```
project-root/
    .git/
        config                   # Repository Git configuration
            # Remote URLs and credentials
            # Branch tracking settings
            # Hook configurations

        hooks/
            pre-commit           # Pre-commit validation hook
                # Lint checks before commit
                # Test execution gates
                # Format verification

            commit-msg           # Commit message validation
                # Format enforcement
                # Issue reference checking
                # AI-suggested improvements

            pre-push             # Pre-push validation
                # Branch protection checks
                # CI preview execution
                # Security scanning

    .gitignore                   # Ignore patterns
        # Build artifacts
        # IDE settings (selective)
        # Environment files

    .windsurfrules               # AI Git behavior
        # Commit message style
        # Branch naming conventions
        # PR description format
```

## AI-Assisted Git Features

### Commit Messages
- Auto-generated from staged changes
- Conventional commits format
- Issue/ticket reference suggestions
- Breaking change detection

### Branch Management
- AI-suggested branch names
- Merge conflict assistance
- Rebase guidance
- Branch cleanup recommendations

## Instructions

1. **Configure Git Credentials**
   - Set up SSH or HTTPS authentication
   - Configure credential caching
   - Set up commit signing (optional)

2. **Set Up AI Assistance**
   - Enable commit message suggestions in settings
   - Configure branch naming conventions in .windsurfrules
   - Set up PR template assistance

3. **Install Git Hooks**
   - Add pre-commit validation hook
   - Configure commit-msg format checking
   - Set up pre-push validation gates

4. **Configure Team Standards**
   - Document commit message conventions
   - Define branch naming patterns
   - Create PR templates

5. **Train on Workflow**
   - Let Cascade learn from existing history
   - Refine suggestions based on feedback
   - Update rules as patterns evolve

## Output

- Configured Git hooks
- AI-assisted commit messages
- Branch naming suggestions
- PR descriptions with context

## Error Handling

| Error | Cause | Solution |
|-------|-------|----------|
| Commit message rejected | Format validation failed | Follow conventional commits format |
| Pre-commit hook failed | Lint or test errors | Fix errors before committing |
| Push rejected | Branch protection rules | Create PR or request override |
| Merge conflict | Divergent branches | Use Cascade for conflict resolution assistance |
| Credential error | Auth expired or invalid | Refresh credentials, check SSH keys |

## Examples

**Example: Generate Commit Message**
Request: "Generate commit message for staged changes"
Result: "feat(auth): add OAuth2 support for Google login\n\nImplement Google OAuth2 flow with token refresh.\nCloses #123"

**Example: Resolve Merge Conflict**
Request: "Help resolve this merge conflict in user-service.ts"
Result: Cascade analyzes both versions, suggests resolution based on context

**Example: Create Feature Branch**
Request: "Create branch for user profile feature"
Result: Suggests "feature/user-profile-management" following team conventions

## Resources

- [Windsurf Git Integration](https://docs.windsurf.ai/features/git)
- [Conventional Commits](https://www.conventionalcommits.org/)
- [Git Hooks Documentation](https://git-scm.com/docs/githooks)

## Success Criteria

- Git operations complete successfully
- AI-suggested commit messages accepted 80%+
- Code review cycles shortened by 35%
