---
name: "windsurf-cascade-context"
description: |
  Manage Cascade context window and memory for complex projects. Activate when users mention
  "cascade context", "ai memory", "context management", "large codebase navigation",
  or "multi-session development". Handles context optimization and persistence. Use when working with windsurf cascade context functionality. Trigger with phrases like "windsurf cascade context", "windsurf context", "windsurf".
allowed-tools: Read,Write,Edit,Grep,Glob
version: 1.0.0
license: MIT
author: "Jeremy Longshore <jeremy@intentsolutions.io>"
---

# Windsurf Cascade Context Management

Optimize Cascade context window for large codebases and complex projects.

## Overview

This skill enables advanced context management for Cascade AI in large-scale projects. It covers context prioritization, memory persistence across sessions, and optimization strategies for codebases with hundreds or thousands of files. Proper context management ensures Cascade maintains accurate understanding of your project architecture and conventions during extended development sessions.

## Prerequisites

- Windsurf IDE with Cascade enabled
- Large codebase (50+ files)
- Project documentation available
- Understanding of project architecture
- Clear identification of critical code paths

## Directory Structure

```
project-root/
    .windsurf/
        context/
            project-overview.md      # High-level project context
                # Architecture summary
                # Key components and relationships
                # Technology stack overview

            module-index.md          # Module reference map
                # Directory to module mapping
                # Key files per module
                # Inter-module dependencies

            api-surface.md           # Public API documentation
                # Exported functions and classes
                # API contracts and types
                # Usage examples

            conventions.md           # Coding conventions
                # Naming patterns
                # File organization rules
                # Common patterns and anti-patterns

        memory/
            session-context.json     # Current session state
                # Recently accessed files
                # Active conversation threads
                # Pending operations

            pinned-context.json      # Persistent context items
                # Critical files always in context
                # Key architectural decisions
                # Team agreements

    .windsurfrules                   # Context behavior rules
        # Context prioritization
        # File relevance scoring
        # Memory management preferences
```

## Context Optimization

### Priority Levels
1. **Critical** - Always in context (pinned)
2. **High** - Recent edits and related files
3. **Medium** - Same module files
4. **Low** - Project-wide utilities

### Context Strategies
- Pin architectural decision records
- Include test files with source
- Reference documentation inline
- Maintain dependency graph awareness

## Instructions

1. **Map Project Structure**
   - Create module-index.md with directory mappings
   - Document inter-module dependencies
   - Identify critical code paths

2. **Configure Context Priorities**
   - Pin essential files in pinned-context.json
   - Set relevance weights for file types
   - Configure context window limits

3. **Create Context Documentation**
   - Write project-overview.md with architecture
   - Document conventions in conventions.md
   - Maintain api-surface.md for public interfaces

4. **Optimize for Workflow**
   - Adjust context window size based on needs
   - Configure memory persistence settings
   - Set up context preloading for common tasks

5. **Monitor and Refine**
   - Review context usage patterns
   - Remove stale context items
   - Update priorities based on workflow

## Output

- Optimized context configuration
- Project context documentation
- Module index for navigation
- Session state persistence

## Error Handling

| Error | Cause | Solution |
|-------|-------|----------|
| Context overflow | Too many files loaded | Reduce priority of non-essential files |
| Stale context | Outdated information | Clear session state, refresh context |
| Missing relationships | Incomplete module index | Update module-index.md with dependencies |
| Slow responses | Context too large | Prioritize critical files, remove redundant |
| Cross-module confusion | Missing dependency info | Add inter-module relationships to index |

## Examples

**Example: Configure Large Monorepo**
Request: "Set up context management for our 500+ file monorepo"
Result: Module index with service boundaries, pinned shared utilities, context priorities

**Example: Pin Critical Files**
Request: "Ensure database schema and API types are always in context"
Result: Files added to pinned-context.json with high priority

**Example: Optimize for Backend Work**
Request: "Configure context for backend development focus"
Result: Backend modules prioritized, frontend de-prioritized, API docs pinned

## Resources

- [Windsurf Context Management](https://docs.windsurf.ai/features/context)
- [Large Codebase Best Practices](https://docs.windsurf.ai/guides/large-codebases)
- [Memory Persistence Configuration](https://docs.windsurf.ai/features/memory)

## Success Criteria

- Context maintained across 100+ file references
- Accurate cross-file understanding
- 50% faster complex refactoring
