---
name: "windsurf-api-development"
description: |
  Generate API clients and documentation with Cascade. Activate when users mention
  "generate api client", "api documentation", "openapi generation", "sdk generation",
  or "api integration". Handles API development workflows. Use when working with APIs or building integrations. Trigger with phrases like "windsurf api development", "windsurf development", "windsurf".
allowed-tools: "Read,Write,Edit,Bash(cmd:*),Grep"
version: 1.0.0
license: MIT
author: "Jeremy Longshore <jeremy@intentsolutions.io>"
---

# Windsurf API Development

Generate API clients and documentation with Cascade AI assistance.

## Overview

This skill enables AI-assisted API development workflows within Windsurf. Cascade can generate type-safe API clients from OpenAPI/Swagger specs, create comprehensive API documentation, design REST and GraphQL schemas, and produce SDKs for multiple languages. It accelerates API development from design through implementation to documentation.

## Prerequisites

- Windsurf IDE with Cascade enabled
- OpenAPI/Swagger specification or API endpoints
- Target language runtime (Node.js, Python, etc.)
- Understanding of API design patterns
- Documentation requirements defined

## Directory Structure

```
project-root/
    api/
        specs/
            openapi.yaml                 # OpenAPI specification
                # Endpoint definitions
                # Schema definitions
                # Authentication specs

            graphql.schema.graphql       # GraphQL schema
                # Type definitions
                # Query definitions
                # Mutation definitions

        clients/
            typescript/
                index.ts                 # Generated TypeScript client
                    # API class definition
                    # Method implementations
                    # Type exports

                types.ts                 # Type definitions
                    # Request types
                    # Response types
                    # Error types

            python/
                client.py                # Generated Python client
                    # Client class
                    # Method implementations
                    # Type hints

        docs/
            api-reference.md             # API reference documentation
                # Endpoint descriptions
                # Parameter details
                # Response examples

            getting-started.md           # Quick start guide
                # Installation
                # Authentication
                # First request

    .windsurf/
        api/
            templates/
                client-template.ts       # Client generation template
                    # Class structure
                    # Method patterns
                    # Error handling

                docs-template.md         # Documentation template
                    # Section structure
                    # Example format
                    # Link patterns

            config/
                generation-config.json   # Generation settings
                    # Output paths
                    # Language targets
                    # Style preferences
```

## API Features

### Client Generation
- TypeScript/JavaScript clients
- Python clients
- Type-safe implementations
- Error handling patterns

### Documentation
- OpenAPI/Swagger docs
- Interactive examples
- SDK documentation
- Changelog generation

## Instructions

1. **Define API Specification**
   - Create or import OpenAPI spec
   - Define request/response schemas
   - Document authentication methods

2. **Generate Clients**
   - Select target languages
   - Configure generation options
   - Generate type-safe client code

3. **Implement Endpoints**
   - Use Cascade for endpoint implementation
   - Generate request handlers
   - Add validation and error handling

4. **Create Documentation**
   - Generate API reference docs
   - Add usage examples
   - Create quick start guides

5. **Test and Validate**
   - Run contract tests
   - Validate against specification
   - Test generated clients

## Output

- Generated API clients (TypeScript, Python, etc.)
- Type definitions and schemas
- API reference documentation
- Quick start guides and examples

## Error Handling

| Error | Cause | Solution |
|-------|-------|----------|
| Schema validation failed | Invalid OpenAPI spec | Fix schema errors, validate with tool |
| Type generation error | Unsupported schema construct | Simplify schema or add custom handler |
| Client compile error | Generated code invalid | Review template, fix generation config |
| Doc generation incomplete | Missing descriptions | Add descriptions to OpenAPI spec |
| Contract test failed | Implementation mismatch | Update implementation to match spec |

## Examples

**Example: Generate TypeScript Client**
Request: "Generate TypeScript API client from our OpenAPI spec"
Result: Type-safe client with all endpoints, request/response types, and error handling

**Example: Create API Documentation**
Request: "Generate API documentation with examples"
Result: Markdown docs with endpoint descriptions, parameter tables, and curl examples

**Example: Design REST API**
Request: "Help design REST API for user management"
Result: OpenAPI spec with user CRUD endpoints, authentication, and error responses

## Resources

- [Windsurf API Development](https://docs.windsurf.ai/features/api-development)
- [OpenAPI Specification](https://swagger.io/specification/)
- [API Design Best Practices](https://docs.windsurf.ai/guides/api-design)

## Success Criteria

- Clients pass contract tests
- 100% endpoint coverage
- 75% reduction in integration time
