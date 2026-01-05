---
name: "windsurf-dockerfile-generation"
description: |
  Create optimized Dockerfiles with AI-driven best practices. Activate when users mention
  "create dockerfile", "container image", "docker optimization", "containerize application",
  or "docker best practices". Handles Docker configuration generation. Use when working with windsurf dockerfile generation functionality. Trigger with phrases like "windsurf dockerfile generation", "windsurf generation", "windsurf".
allowed-tools: "Read,Write,Edit,Bash(cmd:*)"
version: 1.0.0
license: MIT
author: "Jeremy Longshore <jeremy@intentsolutions.io>"
---

# Windsurf Dockerfile Generation

Create optimized Dockerfiles with AI-driven best practices.

## Overview

This skill enables AI-assisted Docker configuration within Windsurf. Cascade analyzes your application to generate optimized Dockerfiles with multi-stage builds, minimal base images, proper layer caching, and security best practices. It supports Node.js, Python, Go, Java, and other common runtimes with framework-specific optimizations.

## Prerequisites

- Windsurf IDE with Cascade enabled
- Docker installed locally
- Application with defined dependencies
- Understanding of containerization concepts
- Target deployment environment defined

## Directory Structure

```
project-root/
    Dockerfile                       # Production Dockerfile
        # Multi-stage build
        # Minimal base image
        # Security hardening
        # Layer optimization

    Dockerfile.dev                   # Development Dockerfile
        # Development tools included
        # Hot reload support
        # Debugging capabilities

    docker-compose.yml               # Service orchestration
        # Service definitions
        # Network configuration
        # Volume mappings

    docker-compose.dev.yml           # Development overrides
        # Source mounting
        # Port exposures
        # Dev tool containers

    .dockerignore                    # Build context exclusions
        # Node modules
        # Build artifacts
        # Local configuration

    .windsurf/
        docker/
            templates/
                node-app.dockerfile      # Node.js template
                    # Optimal base image selection
                    # Dependency layer caching
                    # Non-root user setup

                python-app.dockerfile    # Python template
                    # Virtual environment
                    # Requirements optimization
                    # Health check patterns

            security-scan.json           # Security checklist
                # Base image vulnerabilities
                # Secret exposure risks
                # Permission issues
```

## Best Practices

### Layer Optimization
- Order commands by change frequency
- Combine RUN statements
- Use .dockerignore effectively
- Leverage build cache

### Security
- Use minimal base images
- Run as non-root user
- Scan for vulnerabilities
- No secrets in images

## Instructions

1. **Analyze Application**
   - Identify runtime and dependencies
   - Map build process steps
   - Document runtime requirements

2. **Select Base Image**
   - Choose minimal appropriate base
   - Consider distroless or alpine variants
   - Check for security vulnerabilities

3. **Generate Dockerfile**
   - Use Cascade for initial generation
   - Apply multi-stage build pattern
   - Optimize layer ordering

4. **Configure Security**
   - Add non-root user
   - Remove unnecessary tools
   - Set appropriate permissions

5. **Test and Validate**
   - Build image locally
   - Check image size
   - Run security scans

## Output

- Optimized production Dockerfile
- Development Dockerfile with dev tools
- docker-compose.yml for orchestration
- .dockerignore for build optimization

## Error Handling

| Error | Cause | Solution |
|-------|-------|----------|
| Build failed | Missing dependencies | Check COPY commands, verify paths |
| Large image size | Unoptimized layers | Use multi-stage, add .dockerignore |
| Permission denied | Wrong user context | Set proper USER and permissions |
| Cache not working | Layer ordering | Reorder commands, dependencies first |
| Security scan fails | Vulnerable base | Update base image, patch vulnerabilities |

## Examples

**Example: Generate Node.js Dockerfile**
Request: "Create optimized Dockerfile for our Express.js API"
Result: Multi-stage build with npm ci, non-root user, alpine base

**Example: Python ML Application**
Request: "Containerize our Python machine learning service"
Result: Multi-stage build with virtual env, optimized requirements, GPU support

**Example: Development Setup**
Request: "Create Docker setup for local development with hot reload"
Result: Dockerfile.dev with mounted volumes, docker-compose.dev.yml

## Resources

- [Windsurf Docker Guide](https://docs.windsurf.ai/features/docker)
- [Docker Best Practices](https://docs.docker.com/develop/develop-images/dockerfile_best-practices/)
- [Container Security Guide](https://docs.windsurf.ai/guides/container-security)

## Success Criteria

- Successful build on first attempt
- Minimal image size
- Security best practices applied
- 70% reduction in build failures
