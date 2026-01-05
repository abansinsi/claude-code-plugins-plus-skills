---
name: "cursor-api-key-management"
description: |
  Manage API keys and authentication in Cursor. Triggers on "cursor api key",
  "cursor openai key", "cursor anthropic key", "own api key cursor". Use when working with APIs or building integrations. Trigger with phrases like "cursor api key management", "cursor management", "cursor".
allowed-tools: "Read, Write, Edit, Bash(cmd:*)"
version: 1.0.0
license: MIT
author: "Jeremy Longshore <jeremy@intentsolutions.io>"
---

# Cursor API Key Management

## Overview

### Why Use Your Own API Keys?
```
Benefits:
- Bypass Cursor rate limits
- Access specific models
- Control costs directly
- Use enterprise agreements
- Comply with data policies

Considerations:
- You pay API provider directly
- Need to manage keys securely
- May lose some Cursor optimizations
```

## Supported Providers

### OpenAI
```json
// Settings > Cursor > API Keys

{
  "cursor.openai.apiKey": "sk-...",
  "cursor.openai.organization": "org-..." // optional
}

Available models with your key:
- gpt-4-turbo
- gpt-4
- gpt-4-32k
- gpt-3.5-turbo
- gpt-3.5-turbo-16k
```

### Anthropic
```json
{
  "cursor.anthropic.apiKey": "sk-ant-..."
}

Available models:
- claude-3-opus
- claude-3-sonnet
- claude-3-haiku
- claude-2.1
```

### Azure OpenAI
```json
{
  "cursor.azure.apiKey": "...",
  "cursor.azure.endpoint": "https://YOUR-RESOURCE.openai.azure.com",
  "cursor.azure.deployment": "gpt-4"
}

Benefits:
- Enterprise security
- Regional data residency
- Private network support
- Azure AD authentication
```

### Google AI (Gemini)
```json
{
  "cursor.google.apiKey": "...",
  "cursor.google.model": "gemini-pro"
}
```

## Configuration Methods

### Via Settings UI
```
1. Open Settings (Cmd+,)
2. Search for "Cursor API"
3. Enter your API key
4. Save and restart if prompted
```

### Via settings.json
```json
// ~/.config/Cursor/User/settings.json

{
  "cursor.apiKeys": {
    "openai": "sk-...",
    "anthropic": "sk-ant-...",
    "azure": {
      "apiKey": "...",
      "endpoint": "https://...",
      "deployment": "..."
    }
  }
}
```

### Via Environment Variables
```bash
# Shell profile (~/.zshrc or ~/.bashrc)
export OPENAI_API_KEY="sk-..."
export ANTHROPIC_API_KEY="sk-ant-..."

# Then in settings.json:
{
  "cursor.openai.apiKey": "${OPENAI_API_KEY}",
  "cursor.anthropic.apiKey": "${ANTHROPIC_API_KEY}"
}
```

## Security Best Practices

### Secure Storage
```
DO:
- Use environment variables
- Use secrets managers
- Encrypt backup files
- Restrict file permissions

DON'T:
- Hardcode in settings.json
- Commit to version control
- Share in plain text
- Use in screenshots
```

### File Permissions
```bash
# Secure settings file
chmod 600 ~/.config/Cursor/User/settings.json

# Verify permissions
ls -la ~/.config/Cursor/User/settings.json
# Should show: -rw------- (owner read/write only)
```

### Key Rotation
```
Regular rotation schedule:
- Development keys: Every 90 days
- Production keys: Every 30 days
- After any potential exposure: Immediately

Rotation process:
1. Generate new key from provider
2. Update in Cursor settings
3. Verify functionality
4. Revoke old key
5. Document rotation
```

## Cost Management

### Monitoring Usage
```
OpenAI Dashboard:
- platform.openai.com/usage
- View daily/monthly usage
- Set billing alerts
- Check per-model costs

Anthropic Console:
- console.anthropic.com
- Usage analytics
- Cost breakdown
```

### Setting Limits
```
OpenAI:
- Set monthly budget cap
- Configure billing alerts
- Enable hard limits

Azure:
- Set spending limits
- Configure alerts
- Use Azure Cost Management
```

### Cost Optimization
```
Strategies:
1. Use appropriate model for task
   - GPT-3.5 for simple completions
   - GPT-4 only when needed

2. Reduce context size
   - Select less code
   - Be specific in prompts

3. Cache common patterns
   - Use .cursorrules effectively
   - Reduce repeated queries
```

## Troubleshooting

### "Invalid API Key"
```
Checklist:
[ ] Key is correctly copied (no extra spaces)
[ ] Key hasn't expired
[ ] Key has required permissions
[ ] Correct provider selected
[ ] Account is active

Test key:
curl https://api.openai.com/v1/models \
  -H "Authorization: Bearer sk-..."
```

### "Rate Limited"
```
Solutions:
1. Check rate limits for your tier
2. Upgrade API plan if needed
3. Reduce request frequency
4. Use caching/debouncing
```

### "Model Not Available"
```
Causes:
- Model requires waitlist access
- Model not available in your region
- Wrong model name

Verify:
1. Check provider documentation
2. Confirm model access in dashboard
3. Try different model
```

### "Insufficient Quota"
```
Solutions:
1. Add billing to API account
2. Increase spending limit
3. Check for free tier exhaustion
4. Upgrade to paid plan
```

## Team Key Management

### Shared Keys (Not Recommended)
```
Issues with shared keys:
- No individual tracking
- Security risk
- Hard to rotate
- Compliance problems
```

### Per-User Keys
```
Best practice:
1. Each developer has own key
2. Keys tied to individual accounts
3. Usage tracked per person
4. Easy rotation
```

### Enterprise Setup
```
Options:
1. Azure OpenAI (enterprise)
   - Central management
   - Azure AD auth
   - RBAC controls

2. API Gateway
   - Centralized key management
   - Usage tracking
   - Rate limiting

3. Secrets Manager
   - HashiCorp Vault
   - AWS Secrets Manager
   - Azure Key Vault
```

## Backup and Recovery

### Key Backup
```bash
# Secure backup (encrypted)
gpg --symmetric --output cursor-keys.gpg <<EOF
OPENAI_API_KEY=sk-...
ANTHROPIC_API_KEY=sk-ant-...
EOF

# Decrypt when needed
gpg --decrypt cursor-keys.gpg
```

### Recovery Procedure
```
If key is lost:
1. Generate new key from provider
2. Update Cursor settings
3. Test functionality
4. Update backups
5. Revoke old key if found
```

## Compliance Considerations

### Audit Trail
```
Track:
- When keys were created
- Who has access
- When rotated
- Usage patterns

Document:
- Key management policy
- Rotation schedule
- Access controls
- Incident response
```

### Regulatory Requirements
```
HIPAA/PCI/SOC2:
- Encrypt keys at rest
- Audit access
- Regular rotation
- Access controls
- Incident procedures
```

## Prerequisites

- Cursor IDE Pro or Business subscription (or own API keys)
- API account with OpenAI, Anthropic, Azure, or Google
- API key with appropriate permissions and credits
- Secure storage solution for credentials

## Instructions

1. Generate API key from your chosen provider
2. Open Cursor Settings (Cmd+,)
3. Search for "Cursor API"
4. Enter your API key in the appropriate field
5. Set file permissions to restrict access
6. Configure billing alerts on provider dashboard
7. Test API key by making a request in Cursor

## Output

- Custom API key configured in Cursor
- Bypass of Cursor rate limits
- Direct billing relationship with provider
- Access to specific models via your key

## Error Handling

| Error | Cause | Solution |
|-------|-------|----------|
| Invalid API Key | Key expired or miscopied | Verify key format and regenerate if needed |
| Rate Limited | Exceeded tier limits | Wait for reset or upgrade API plan |
| Model Not Available | Model requires special access | Check provider dashboard for model access |
| Insufficient Quota | No credits or billing not set | Add payment method to API account |

## Examples

**Example: Configure OpenAI API Key**
Request: "Set up my OpenAI API key for Cursor"
Result: OpenAI key configured in settings, GPT-4 models accessible via personal key

**Example: Rotate Expired API Keys**
Request: "Help me rotate my Anthropic API key"
Result: New key generated, updated in Cursor settings, old key revoked

## Resources

- [OpenAI API Keys](https://platform.openai.com/api-keys)
- [Anthropic Console](https://console.anthropic.com/)
- [Azure OpenAI Service](https://azure.microsoft.com/en-us/products/ai-services/openai-service)
- [Cursor Security Documentation](https://cursor.com/security)
