---
name: "windsurf-code-completion"
description: |
  Configure and optimize Supercomplete code suggestions. Activate when users mention
  "code completion", "autocomplete", "supercomplete", "inline suggestions",
  or "ai completions". Handles completion configuration and optimization. Use when working with windsurf code completion functionality. Trigger with phrases like "windsurf code completion", "windsurf completion", "windsurf".
allowed-tools: Read,Write,Edit
version: 1.0.0
license: MIT
author: "Jeremy Longshore <jeremy@intentsolutions.io>"
---

# Windsurf Code Completion

Configure and optimize Supercomplete for maximum productivity.

## Overview

This skill enables configuration and optimization of Windsurf's Supercomplete AI-powered code completion. Supercomplete provides intelligent, context-aware suggestions that go beyond traditional autocomplete. It understands your codebase patterns, follows your conventions, and can complete multi-line blocks of code. Proper configuration ensures relevant, fast suggestions that match your coding style.

## Prerequisites

- Windsurf IDE installed and running
- Active Cascade AI subscription
- Project with code to analyze
- Understanding of coding patterns in project
- Language server enabled for target languages

## Directory Structure

```
project-root/
    .windsurf/
        completion/
            preferences.json         # Completion behavior settings
                # Trigger delay configuration
                # Suggestion quantity limits
                # Context window size

            language-config/
                typescript.json      # TypeScript-specific settings
                    # Type inference depth
                    # Import suggestion behavior
                    # JSDoc completion

                python.json          # Python-specific settings
                    # Type hint suggestions
                    # Docstring completion
                    # Import organization

                rust.json            # Rust-specific settings
                    # Lifetime suggestion behavior
                    # Macro expansion
                    # Cargo integration

            snippets/
                custom-snippets.json # User-defined completions
                    # Project-specific patterns
                    # Boilerplate templates
                    # Common code blocks

    .windsurfrules                   # AI completion guidance
        # Code style for suggestions
        # Naming convention preferences
        # Pattern priorities
```

## Completion Features

### Supercomplete
- Multi-line intelligent completions
- Context-aware suggestions
- Import auto-resolution
- Type inference integration

### Configuration Options
- Trigger sensitivity
- Suggestion ranking
- Inline vs popup display
- Tab/Enter acceptance

## Instructions

1. **Configure Trigger Behavior**
   - Set trigger delay (faster for experienced users)
   - Define trigger characters per language
   - Configure minimum context requirements

2. **Set Up Language-Specific Options**
   - Enable relevant language servers
   - Configure type inference settings
   - Set import suggestion preferences

3. **Create Custom Snippets**
   - Add project-specific patterns
   - Define boilerplate templates
   - Configure expansion triggers

4. **Optimize Performance**
   - Adjust context window size
   - Configure suggestion caching
   - Set resource limits

5. **Personalize Experience**
   - Train on codebase patterns
   - Adjust ranking weights
   - Configure acceptance shortcuts

## Output

- Configured completion preferences
- Language-specific settings
- Custom snippet library
- Optimized completion experience

## Error Handling

| Error | Cause | Solution |
|-------|-------|----------|
| No completions appearing | Language server not running | Start language server, check logs |
| Slow completions | Large context or network | Reduce context window, check connection |
| Irrelevant suggestions | Missing project context | Add .windsurfrules with patterns |
| Type errors in completions | Incomplete type information | Improve type annotations in code |
| Completions cut off | Max length exceeded | Increase suggestion length limit |

## Examples

**Example: Configure TypeScript Completion**
Request: "Optimize code completion for TypeScript with React"
Result: Type inference enabled, JSX snippets, import organization configured

**Example: Create Custom Snippets**
Request: "Add snippet for creating API handlers"
Result: Custom snippet with handler boilerplate, error handling, and types

**Example: Speed Up Completions**
Request: "Make completions appear faster with less delay"
Result: Trigger delay reduced, context optimized, caching enabled

## Resources

- [Windsurf Supercomplete Guide](https://docs.windsurf.ai/features/supercomplete)
- [Language Server Configuration](https://docs.windsurf.ai/features/language-servers)
- [Custom Snippets Reference](https://docs.windsurf.ai/reference/snippets)

## Success Criteria

- Completions appear within 150ms
- 85%+ suggestion acceptance rate
- 60% faster boilerplate writing
