---
name: "windsurf-theme-customization"
description: |
  Configure Windsurf themes and visual settings for accessibility. Activate when users mention
  "change theme", "customize colors", "accessibility settings", "visual preferences",
  or "dark mode". Handles theme configuration and accessibility compliance. Use when working with windsurf theme customization functionality. Trigger with phrases like "windsurf theme customization", "windsurf customization", "windsurf".
allowed-tools: Read,Write,Edit
version: 1.0.0
license: MIT
author: "Jeremy Longshore <jeremy@intentsolutions.io>"
---

# Windsurf Theme Customization

Configure visual settings for accessibility and developer comfort.

## Overview

This skill enables comprehensive theme customization within Windsurf. It covers color schemes, font configurations, UI scaling, and accessibility settings. Proper theme configuration reduces eye strain, improves code readability, and ensures compliance with accessibility standards like WCAG 2.1 for team members with visual impairments.

## Prerequisites

- Windsurf IDE installed
- Understanding of accessibility requirements
- Color vision considerations for team
- Preferred font selections
- Display resolution and scaling needs

## Directory Structure

```
~/.windsurf/
    settings.json                # Global visual settings
        # Color theme selection
        # Font configuration
        # UI scale settings
        # Accessibility options

    themes/
        custom-dark.json         # Custom dark theme
            # Editor colors
            # Syntax highlighting
            # UI element colors
            # Cascade panel styling

        custom-light.json        # Custom light theme
            # High contrast options
            # Reduced eye strain colors
            # Print-friendly settings

project-root/
    .vscode/
        settings.json            # Project theme overrides
            # Workspace-specific colors
            # Language-specific highlighting
            # Semantic token colors

    .windsurfrules               # AI response formatting
        # Code block styling preferences
        # Diff highlighting colors
        # Cascade output formatting
```

## Theme Configuration

### Color Accessibility
- Minimum 4.5:1 contrast ratio for text
- Distinct colors for syntax elements
- Color-blind friendly palettes
- Focus indicators for keyboard navigation

### Font Settings
- Editor font: Monospace with ligature support
- Terminal font: Clear distinction from editor
- UI font: System default or accessible choice
- Font size: Scalable based on preference

## Instructions

1. **Select Base Theme**
   - Choose dark or light as foundation
   - Consider time-of-day auto-switching
   - Test with actual code samples

2. **Configure Colors**
   - Adjust syntax highlighting for visibility
   - Set UI element colors
   - Configure Cascade panel styling

3. **Set Up Fonts**
   - Choose accessible monospace font
   - Configure font size and line height
   - Enable ligatures if desired

4. **Enable Accessibility Features**
   - Configure screen reader support
   - Set up keyboard navigation
   - Enable focus indicators

5. **Verify Compliance**
   - Check contrast ratios with tools
   - Test keyboard navigation
   - Validate with accessibility checker

## Output

- Customized theme configuration
- Font settings optimized for readability
- Accessibility-compliant color scheme
- Cross-panel consistent styling

## Error Handling

| Error | Cause | Solution |
|-------|-------|----------|
| Theme not loading | Invalid JSON syntax | Validate theme file syntax |
| Colors not applying | Cache issue | Reload Windsurf window |
| Font not rendering | Font not installed | Install font or choose alternative |
| Low contrast warning | WCAG violation | Increase contrast ratio |
| UI elements missing | Theme incomplete | Add missing color definitions |

## Examples

**Example: Create High-Contrast Theme**
Request: "Set up high-contrast theme for accessibility"
Result: Theme with WCAG AAA contrast ratios, bold syntax colors

**Example: Configure Dark Theme**
Request: "Customize dark theme to reduce eye strain"
Result: Dark theme with reduced blue light, comfortable syntax colors

**Example: Set Up Font Configuration**
Request: "Configure fonts for dyslexia-friendly reading"
Result: OpenDyslexic or similar font, increased spacing, clear colors

## Resources

- [Windsurf Theme Guide](https://docs.windsurf.ai/features/themes)
- [WCAG 2.1 Guidelines](https://www.w3.org/WAI/WCAG21/quickref/)
- [Accessible Color Palettes](https://docs.windsurf.ai/guides/accessibility)

## Success Criteria

- WCAG 2.1 AA compliance
- Correct rendering across all panels
- Reduced eye strain and fatigue
