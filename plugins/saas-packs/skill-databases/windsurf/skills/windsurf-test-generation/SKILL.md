---
name: "windsurf-test-generation"
description: |
  Generate comprehensive test suites using Cascade. Activate when users mention
  "generate tests", "test coverage", "write unit tests", "create test suite",
  or "tdd assistance". Handles AI-powered test generation. Use when writing or running tests. Trigger with phrases like "windsurf test generation", "windsurf generation", "windsurf".
allowed-tools: "Read,Write,Edit,Bash(cmd:*),Grep,Glob"
version: 1.0.0
license: MIT
author: "Jeremy Longshore <jeremy@intentsolutions.io>"
---

# Windsurf Test Generation

Generate comprehensive test suites using Cascade AI assistance.

## Overview

This skill enables AI-powered test generation for any codebase using Windsurf's Cascade. It analyzes function signatures, identifies edge cases, creates meaningful assertions, and generates mock data. Supports unit tests, integration tests, and component tests across multiple frameworks including Jest, Vitest, Mocha, pytest, and testing-library.

## Prerequisites

- Windsurf IDE with Cascade enabled
- Testing framework installed (Jest, Vitest, pytest, etc.)
- Project with testable code (functions, classes, components)
- Code coverage tool configured (optional but recommended)
- Understanding of testing patterns and best practices

## Directory Structure

```
project-root/
    src/
        components/
            Button.tsx               # Component to test
            Button.test.tsx          # Generated test file
                # Render tests
                # Interaction tests
                # Accessibility tests

        utils/
            formatters.ts            # Utility functions
            formatters.test.ts       # Generated unit tests
                # Input validation tests
                # Edge case coverage
                # Error handling tests

        services/
            api.ts                   # API service
            api.test.ts              # Integration tests
                # Mock setup
                # Request/response tests
                # Error scenario tests

    .windsurf/
        testing/
            templates/
                unit-test.template.ts    # Unit test template
                    # Describe/it structure
                    # Setup and teardown
                    # Assertion patterns

                integration-test.template.ts   # Integration template
                    # Service mocking
                    # Database fixtures
                    # Cleanup procedures

            coverage-config.json         # Coverage requirements
                # Minimum thresholds
                # Exclude patterns
                # Report formats

            test-patterns/
                component-tests.md       # Component test patterns
                    # Rendering tests
                    # Event handling
                    # State changes

                hook-tests.md            # Hook test patterns
                    # renderHook usage
                    # Act and waitFor
                    # Cleanup patterns
```

## Test Generation Features

### Analysis
- Function signature analysis
- Edge case identification
- Dependency detection
- Error path mapping

### Generation
- Test structure scaffolding
- Meaningful assertions
- Mock data creation
- Coverage optimization

## Instructions

1. **Configure Testing Framework**
   - Set up test runner (Jest, Vitest, pytest)
   - Configure mocking libraries (jest.mock, vi.mock)
   - Set coverage thresholds in coverage-config.json

2. **Select Target Code**
   - Open file or select function to test
   - Cascade analyzes signature and dependencies
   - Review detected edge cases and scenarios

3. **Generate Tests with Cascade**
   - Request test generation via Cascade panel
   - Review generated test structure
   - Refine assertions and edge cases

4. **Add Custom Scenarios**
   - Include domain-specific test cases
   - Add integration scenarios
   - Configure mock responses

5. **Integrate into Workflow**
   - Add tests to CI pipeline
   - Set up pre-commit hooks
   - Configure coverage reporting

## Output

- Test files with comprehensive coverage
- Mock data and fixture files
- Coverage report with metrics
- Test pattern documentation for team

## Error Handling

| Error | Cause | Solution |
|-------|-------|----------|
| Mock not working | Incorrect mock path | Verify import path matches mock setup |
| Async test timeout | Missing await or done() | Add proper async handling |
| Coverage below threshold | Missing test cases | Generate additional edge case tests |
| Type error in test | Mock type mismatch | Update mock types to match interface |
| Test isolation failure | Shared state between tests | Add proper beforeEach/afterEach cleanup |

## Examples

**Example: Generate Unit Tests for Utility Function**
Request: "Generate tests for the formatCurrency function"
Result: Tests for valid inputs, edge cases (zero, negative, large numbers), invalid inputs, and localization

**Example: Generate Component Tests**
Request: "Create tests for the LoginForm component"
Result: Render tests, user interaction tests, validation tests, and accessibility tests

**Example: Generate API Integration Tests**
Request: "Write integration tests for the UserService API calls"
Result: Success response tests, error handling tests, and timeout/retry tests with mocked responses

## Resources

- [Windsurf Test Generation Guide](https://docs.windsurf.ai/features/test-generation)
- [Jest Documentation](https://jestjs.io/docs/getting-started)
- [Testing Library Best Practices](https://testing-library.com/docs/guiding-principles)

## Success Criteria

- 80%+ code coverage achieved
- Meaningful assertions (not just coverage)
- 65% reduction in test writing time
