---
name: "windsurf-flows-automation"
description: |
  Create and manage Windsurf Flows for repetitive tasks. Activate when users mention
  "windsurf flows", "task automation", "workflow automation", "repetitive tasks",
  or "process automation". Handles Flow creation and management. Use when working with windsurf flows automation functionality. Trigger with phrases like "windsurf flows automation", "windsurf automation", "windsurf".
allowed-tools: "Read,Write,Edit,Bash(cmd:*)"
version: 1.0.0
license: MIT
author: "Jeremy Longshore <jeremy@intentsolutions.io>"
---

# Windsurf Flows Automation

Create and manage Flows to automate repetitive development tasks.

## Overview

This skill enables creation and management of Windsurf Flows - automated workflows that handle repetitive development tasks. Flows can scaffold components, generate boilerplate, run test sequences, and execute multi-step operations with a single command. They combine Cascade AI intelligence with deterministic automation for reliable, repeatable results.

## Prerequisites

- Windsurf IDE with Cascade enabled
- Understanding of repetitive tasks to automate
- Project templates and patterns documented
- Test scenarios for flow validation
- Team agreement on automation standards

## Directory Structure

```
project-root/
    .windsurf/
        flows/
            flow-registry.json       # Registered flows index
                # Flow names and descriptions
                # Trigger conditions
                # Execution statistics

            definitions/
                create-component.flow.json   # Component creation flow
                    # Steps: template, naming, imports
                    # Variable substitutions
                    # Post-creation tasks

                test-coverage.flow.json      # Test coverage flow
                    # Find untested functions
                    # Generate test templates
                    # Run coverage report

                refactor-extract.flow.json   # Extract refactoring flow
                    # Select code block
                    # Create new module
                    # Update imports

            templates/
                component-template.tsx   # Component boilerplate
                    # Parameterized template
                    # Style includes
                    # Test file companion

                hook-template.ts         # Custom hook template
                    # State management
                    # Effect patterns
                    # Return type structure

            logs/
                execution-log.json       # Flow execution history
                    # Timestamps and outcomes
                    # Error details
                    # Rollback markers
```

## Flow Types

### Creation Flows
- Component generation
- Module scaffolding
- Test file creation
- Documentation generation

### Transformation Flows
- Code refactoring patterns
- Migration scripts
- Format conversions
- Batch updates

## Instructions

1. **Identify Repetitive Tasks**
   - Audit daily development workflows
   - Measure time spent on repeated tasks
   - Document manual step sequences

2. **Design Flow Structure**
   - Define step sequence and order
   - Identify required inputs and variables
   - Plan error handling and rollback

3. **Create Flow Definitions**
   - Write flow.json configuration
   - Create template files referenced by flow
   - Add variable placeholders

4. **Test and Validate**
   - Run flow in sandbox mode
   - Verify outputs match expectations
   - Test error scenarios and rollback

5. **Deploy and Monitor**
   - Register flow in flow-registry.json
   - Enable for team use
   - Monitor execution statistics

## Output

- Flow definition files
- Reusable template library
- Execution logs for audit
- Rollback capabilities

## Error Handling

| Error | Cause | Solution |
|-------|-------|----------|
| Flow step failed | Invalid input or state | Check prerequisites, validate inputs |
| Template not found | Missing template file | Verify template path in flow definition |
| Variable undefined | Missing required input | Add variable to flow inputs |
| Rollback failed | Partial state | Manual cleanup using execution log |
| Permission denied | File access restricted | Check file permissions, run with proper access |

## Examples

**Example: Create Component Flow**
Request: "Set up a flow to create React components with tests"
Result: Flow that creates component file, test file, story file, and updates index

**Example: Test Coverage Flow**
Request: "Automate finding and testing uncovered functions"
Result: Flow that scans coverage, identifies gaps, and generates test stubs

**Example: API Endpoint Flow**
Request: "Create flow for adding new API endpoints"
Result: Flow that creates route, handler, types, tests, and documentation

## Resources

- [Windsurf Flows Guide](https://docs.windsurf.ai/features/flows)
- [Flow Definition Reference](https://docs.windsurf.ai/reference/flows)
- [Template Authoring](https://docs.windsurf.ai/guides/templates)

## Success Criteria

- Flows execute reliably
- Rollback capability working
- 10+ hours saved per developer monthly
