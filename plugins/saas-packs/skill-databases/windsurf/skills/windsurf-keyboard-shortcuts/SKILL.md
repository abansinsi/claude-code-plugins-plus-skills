---
name: "windsurf-keyboard-shortcuts"
description: |
  Configure custom keyboard shortcuts for Cascade and AI features. Activate when users mention
  "keyboard shortcuts", "keybindings", "hotkeys", "shortcut configuration",
  or "customize shortcuts". Handles keybinding setup and optimization. Use when working with windsurf keyboard shortcuts functionality. Trigger with phrases like "windsurf keyboard shortcuts", "windsurf shortcuts", "windsurf".
allowed-tools: Read,Write,Edit
version: 1.0.0
license: MIT
author: "Jeremy Longshore <jeremy@intentsolutions.io>"
---

# Windsurf Keyboard Shortcuts

Configure efficient keyboard shortcuts for AI-assisted development workflows.

## Overview

This skill enables customization of Windsurf keyboard shortcuts for optimal productivity. It covers Cascade AI shortcuts, multi-file editing commands, navigation keys, and custom workflow bindings. Proper shortcut configuration can significantly reduce context switching and accelerate common development tasks.

## Prerequisites

- Windsurf IDE installed
- Understanding of current shortcut usage
- Keyboard layout knowledge (QWERTY, etc.)
- Access to settings file
- List of frequently used operations

## Directory Structure

```
~/.windsurf/
    keybindings.json             # Custom keyboard shortcuts
        # Cascade activation shortcuts
        # AI feature quick access
        # Custom workflow bindings
        # Override default bindings

    User/
        keybindings.json         # User-level shortcuts
            # Personal preferences
            # Platform-specific bindings
            # Conflict resolutions

project-root/
    .vscode/
        keybindings.json         # Project-specific shortcuts
            # Team-standard bindings
            # Project workflow shortcuts
            # Task automation triggers

    docs/
        shortcuts-reference.md   # Team shortcut documentation
            # Quick reference card
            # Category groupings
            # Common workflows
```

## Essential Shortcuts

### Cascade AI
- `Cmd/Ctrl + K` - Open Cascade panel
- `Cmd/Ctrl + Shift + K` - Cascade with selection
- `Cmd/Ctrl + L` - Inline completion accept
- `Escape` - Dismiss Cascade suggestions

### Multi-file Operations
- `Cmd/Ctrl + Shift + E` - Apply multi-file edit
- `Cmd/Ctrl + .` - Quick fix with AI
- `F2` - AI-assisted rename

### Navigation
- `Cmd/Ctrl + P` - Quick file open
- `Cmd/Ctrl + Shift + F` - AI-enhanced search
- `Cmd/Ctrl + G` - Go to line with context

## Instructions

1. **Review Default Shortcuts**
   - Document current shortcut bindings
   - Identify conflicts with other tools
   - List shortcuts that conflict with muscle memory

2. **Plan Customizations**
   - Map frequently used operations
   - Design ergonomic key combinations
   - Group related actions on adjacent keys

3. **Configure AI Shortcuts**
   - Set Cascade activation keys
   - Configure completion accept/reject
   - Add context-specific AI triggers

4. **Create Custom Bindings**
   - Add workflow-specific shortcuts
   - Set up macro-like key sequences
   - Configure project-specific bindings

5. **Document and Share**
   - Create team shortcut reference
   - Share keybindings.json with team
   - Set up sync for consistency

## Output

- Customized keybindings.json
- Shortcut reference documentation
- Conflict-free keyboard mappings
- Team-standard shortcut configuration

## Error Handling

| Error | Cause | Solution |
|-------|-------|----------|
| Shortcut not working | Conflict with extension | Disable conflicting binding |
| Shortcut conflict | Multiple bindings | Prioritize or change one binding |
| OS shortcut override | System-level binding | Use different key combination |
| Context mismatch | Wrong editor context | Add when clause to binding |
| Shortcut not registered | Invalid keybindings.json | Validate JSON syntax |

## Examples

**Example: Configure Cascade Shortcuts**
Request: "Set up convenient shortcuts for Cascade panel"
Result: Cmd+K for panel, Cmd+Shift+K for selection, Cmd+Enter to send

**Example: Create Workflow Shortcuts**
Request: "Add shortcut for running tests on current file"
Result: Cmd+Shift+T bound to run test command with current file argument

**Example: Resolve Shortcut Conflict**
Request: "Cmd+K conflicts with my terminal binding"
Result: Cascade moved to Cmd+J, terminal kept on Cmd+K

## Resources

- [Windsurf Keyboard Shortcuts](https://docs.windsurf.ai/features/shortcuts)
- [Key Binding Reference](https://docs.windsurf.ai/reference/keybindings)
- [Ergonomic Shortcut Design](https://docs.windsurf.ai/guides/ergonomics)

## Success Criteria

- All shortcuts functional without conflicts
- Sub-100ms response times
- 25% increase in coding velocity
