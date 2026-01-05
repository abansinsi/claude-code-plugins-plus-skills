---
name: "windsurf-custom-prompts"
description: |
  Create and manage custom prompt libraries for Cascade. Activate when users mention
  "custom prompts", "prompt library", "prompt templates", "cascade prompts",
  or "prompt management". Handles prompt library creation and organization. Use when working with windsurf custom prompts functionality. Trigger with phrases like "windsurf custom prompts", "windsurf prompts", "windsurf".
allowed-tools: Read,Write,Edit,Grep,Glob
version: 1.0.0
license: MIT
author: "Jeremy Longshore <jeremy@intentsolutions.io>"
---

# Windsurf Custom Prompts

Create and manage custom prompt libraries for team knowledge sharing.

## Overview

This skill enables creation and management of custom prompt libraries for Cascade. Teams can build reusable prompt templates for common tasks like code generation, code review, documentation, and debugging. Prompts can include project-specific context and be shared across the organization for consistent AI interactions.

## Prerequisites

- Windsurf IDE with Cascade enabled
- Understanding of effective prompting techniques
- Project conventions documented
- Team agreement on prompt standards
- Use cases identified for automation

## Directory Structure

```
project-root/
    .windsurf/
        prompts/
            library/
                index.json               # Prompt library index
                    # Prompt categories
                    # Search metadata
                    # Usage statistics

                code-generation/
                    react-component.prompt.md    # React component prompt
                        # Component structure
                        # Props definition
                        # Style integration

                    api-endpoint.prompt.md       # API endpoint prompt
                        # Route definition
                        # Handler structure
                        # Error handling

                    database-query.prompt.md     # Query generation prompt
                        # Schema context
                        # Optimization hints
                        # Safety checks

                code-review/
                    security-review.prompt.md    # Security review prompt
                        # Vulnerability checklist
                        # Best practice validation
                        # Fix suggestions

                    performance-review.prompt.md # Performance review prompt
                        # Bottleneck identification
                        # Optimization opportunities
                        # Benchmark comparison

                documentation/
                    api-docs.prompt.md           # API documentation prompt
                        # OpenAPI generation
                        # Example creation
                        # Error documentation

                    readme.prompt.md             # README generation prompt
                        # Project description
                        # Installation steps
                        # Usage examples

            variables/
                project-context.json         # Project-specific variables
                    # Framework name
                    # Coding standards
                    # Team preferences

                tech-stack.json              # Technology stack variables
                    # Languages
                    # Frameworks
                    # Tools

            favorites.json                   # Frequently used prompts
                # Quick access list
                # Usage counts
                # Last used timestamps
```

## Prompt Features

### Organization
- Category-based structure
- Tag-based search
- Usage tracking
- Version history

### Sharing
- Team libraries
- Personal collections
- Import/export
- Sync across devices

## Instructions

1. **Plan Prompt Library**
   - Identify common use cases
   - Define category structure
   - Document prompt requirements

2. **Create Prompt Templates**
   - Write effective prompt instructions
   - Include project context placeholders
   - Add example inputs/outputs

3. **Configure Variables**
   - Define project-specific variables
   - Set up technology stack context
   - Create reusable substitutions

4. **Organize and Index**
   - Categorize prompts logically
   - Add search metadata
   - Tag for discoverability

5. **Enable Team Sharing**
   - Share library with team
   - Set up sync mechanism
   - Track usage for optimization

## Output

- Organized prompt library
- Reusable prompt templates
- Variable configuration files
- Usage statistics and favorites

## Error Handling

| Error | Cause | Solution |
|-------|-------|----------|
| Variable not found | Missing variable definition | Add to project-context.json |
| Prompt too long | Exceeds context limit | Summarize or split prompt |
| Inconsistent results | Vague instructions | Add specific examples and constraints |
| Search not finding prompt | Missing metadata | Update index.json with tags |
| Sync conflict | Concurrent edits | Resolve manually, use version control |

## Examples

**Example: Create Component Prompt**
Request: "Set up a prompt for generating React components"
Result: Template with props interface, JSX structure, and styling patterns

**Example: Security Review Prompt**
Request: "Create prompt for security code reviews"
Result: Checklist-based prompt with OWASP patterns and fix suggestions

**Example: Documentation Prompt**
Request: "Build prompt for generating API documentation"
Result: Template that produces OpenAPI-compatible endpoint descriptions

## Resources

- [Windsurf Prompt Library](https://docs.windsurf.ai/features/prompts)
- [Effective Prompting Guide](https://docs.windsurf.ai/guides/prompting)
- [Team Prompt Sharing](https://docs.windsurf.ai/admin/prompt-sharing)

## Success Criteria

- 95%+ precision on context retrieval
- Reusable prompts across team
- Knowledge captured and shared
