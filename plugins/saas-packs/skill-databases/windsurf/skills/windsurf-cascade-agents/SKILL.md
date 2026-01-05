---
name: "windsurf-cascade-agents"
description: |
  Create custom Cascade agent configurations for specialized tasks. Activate when users mention
  "custom cascade agent", "specialized ai agent", "domain-specific cascade", "agent configuration",
  or "custom ai behavior". Handles custom agent creation and configuration. Use when working with windsurf cascade agents functionality. Trigger with phrases like "windsurf cascade agents", "windsurf agents", "windsurf".
allowed-tools: "Read,Write,Edit,Bash(cmd:*),Grep,Glob"
version: 1.0.0
license: MIT
author: "Jeremy Longshore <jeremy@intentsolutions.io>"
---

# Windsurf Cascade Agents

Create custom Cascade agent configurations for domain-specific tasks.

## Overview

This skill enables creation of specialized Cascade agents tailored for specific domains or tasks. Custom agents can be configured with domain knowledge, specialized prompts, and focused capabilities. Use cases include security review agents, API design agents, performance optimization agents, and documentation writers that understand your project's specific conventions and requirements.

## Prerequisites

- Windsurf IDE with Cascade Pro or Enterprise
- Understanding of prompt engineering principles
- Domain knowledge to encode in agent context
- Project documentation and conventions documented
- Test scenarios for agent validation

## Directory Structure

```
project-root/
    .windsurf/
        agents/
            registry.json                # Agent registry
                # Available agents
                # Activation triggers
                # Priority ordering

            definitions/
                security-reviewer.agent.json     # Security review agent
                    # Security-focused prompts
                    # Vulnerability patterns
                    # Compliance checks

                api-designer.agent.json          # API design agent
                    # REST/GraphQL patterns
                    # Schema validation
                    # Documentation generation

                performance-optimizer.agent.json # Performance agent
                    # Profiling integration
                    # Optimization patterns
                    # Benchmark comparison

                documentation-writer.agent.json  # Docs agent
                    # Documentation style
                    # API documentation
                    # User guide generation

            contexts/
                shared-context.md            # Common context for all agents
                    # Project overview
                    # Team conventions
                    # Technology stack

                security-context.md          # Security agent context
                    # Security requirements
                    # Threat model
                    # Compliance standards

                api-context.md               # API agent context
                    # API conventions
                    # Schema standards
                    # Versioning policies

            prompts/
                system-prompts/
                    security-system.md       # Security agent system prompt
                    api-system.md            # API agent system prompt
                    performance-system.md    # Performance agent system prompt

                user-templates/
                    review-request.md        # Review request template
                    design-request.md        # Design request template
                    optimize-request.md      # Optimization request template
```

## Agent Features

### Domain Specialization
- Security-focused analysis
- API design patterns
- Performance optimization
- Documentation generation

### Context Management
- Persistent domain knowledge
- Project-specific patterns
- Team conventions integration
- Cross-agent context sharing

## Instructions

1. **Define Agent Purpose**
   - Identify the specialized domain or task
   - Document required domain knowledge
   - Set behavior guidelines and constraints

2. **Create System Prompt**
   - Write comprehensive system prompt
   - Include domain expertise and conventions
   - Define output format expectations

3. **Configure Context Sources**
   - Reference project documentation
   - Include relevant code patterns
   - Add team conventions and standards

4. **Set Activation Triggers**
   - Define keywords that activate the agent
   - Configure context patterns for auto-activation
   - Set priority ordering for multiple agents

5. **Test and Refine**
   - Run test scenarios with sample inputs
   - Gather feedback on agent responses
   - Iterate on prompts until accurate

## Output

- Custom agent configurations in registry
- Domain-specific system prompts
- Context files with specialized knowledge
- Activation trigger mappings

## Error Handling

| Error | Cause | Solution |
|-------|-------|----------|
| Agent not activating | Trigger keywords not matching | Review and expand trigger patterns |
| Incorrect domain response | Missing context | Add more domain knowledge to context |
| Context overflow | Too much context loaded | Prioritize essential context, remove redundant |
| Conflicting agents | Multiple agents triggered | Adjust priority ordering in registry |
| Hallucinated information | Insufficient grounding | Add explicit facts and constraints |

## Examples

**Example: Create Security Review Agent**
Request: "Set up a security review agent that checks for OWASP vulnerabilities"
Result: Agent with OWASP context, vulnerability patterns, and security-focused prompts

**Example: Create API Design Agent**
Request: "Configure an agent for REST API design following our conventions"
Result: Agent with API standards, schema patterns, and documentation generation

**Example: Create Documentation Agent**
Request: "Build a documentation agent that writes in our team's style"
Result: Agent with writing guidelines, template formats, and example documentation

## Resources

- [Windsurf Custom Agents Guide](https://docs.windsurf.ai/features/custom-agents)
- [Prompt Engineering Best Practices](https://docs.windsurf.ai/guides/prompt-engineering)
- [Agent Context Management](https://docs.windsurf.ai/features/context-management)

## Success Criteria

- 90%+ accuracy on domain-specific prompts
- Appropriate agent activation
- Specialized workflows enabled
