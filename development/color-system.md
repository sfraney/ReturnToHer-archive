# Color System Documentation

## Overview
This document outlines the comprehensive color system for the "Return to Her" website, providing guidelines for consistent and accessible color usage across all components.

## Color Palette

### Primary Colors (Blue)
**Purpose**: Professional, trustworthy, main brand color
- **50**: `#f0f9ff` - Very light blue (backgrounds, subtle highlights)
- **100**: `#e0f2fe` - Light blue (hover states, light backgrounds)
- **200**: `#bae6fd` - Soft blue (borders, dividers)
- **300**: `#7dd3fc` - Medium light blue (icons, secondary elements)
- **400**: `#38bdf8` - Medium blue (accent elements)
- **500**: `#3b82f6` - Primary blue (main brand color)
- **600**: `#2563eb` - Dark blue (buttons, links)
- **700**: `#1d4ed8` - Darker blue (hover states, emphasis)
- **800**: `#1e40af` - Very dark blue (text on light backgrounds)
- **900**: `#1e3a8a` - Darkest blue (headings, strong emphasis)

### Secondary Colors (Purple)
**Purpose**: Creative, spiritual, complements primary theme
- **50**: `#fdf4ff` - Very light purple (backgrounds, subtle highlights)
- **100**: `#fae8ff` - Light purple (hover states, light backgrounds)
- **200**: `#f5d0fe` - Soft purple (borders, dividers)
- **300**: `#f0abfc` - Medium light purple (icons, secondary elements)
- **400**: `#e879f9` - Medium purple (accent elements)
- **500**: `#a855f7` - Primary purple (secondary brand color)
- **600**: `#9333ea` - Dark purple (buttons, links)
- **700**: `#7c3aed` - Darker purple (hover states, emphasis)
- **800**: `#6b21a8` - Very dark purple (text on light backgrounds)
- **900**: `#581c87` - Darkest purple (headings, strong emphasis)

### Semantic Colors

#### Success (Green)
**Purpose**: Positive actions, confirmations, success states
- **50**: `#f0fdf4` - Very light green (success backgrounds)
- **500**: `#22c55e` - Success green (success indicators)
- **600**: `#16a34a` - Dark success (success text)
- **700**: `#15803d` - Darker success (emphasis)

#### Warning (Orange)
**Purpose**: Caution, warnings, attention needed
- **50**: `#fffbeb` - Very light orange (warning backgrounds)
- **500**: `#f59e0b` - Warning orange (warning indicators)
- **600**: `#d97706` - Dark warning (warning text)
- **700**: `#b45309` - Darker warning (emphasis)

#### Error (Red)
**Purpose**: Errors, destructive actions, critical issues
- **50**: `#fef2f2` - Very light red (error backgrounds)
- **500**: `#ef4444` - Error red (error indicators)
- **600**: `#dc2626` - Dark error (error text)
- **700**: `#b91c1c` - Darker error (emphasis)

#### Info (Blue)
**Purpose**: Information, neutral states, general messaging
- **50**: `#eff6ff` - Very light blue (info backgrounds)
- **500**: `#3b82f6` - Info blue (info indicators)
- **600**: `#2563eb` - Dark info (info text)
- **700**: `#1d4ed8` - Darker info (emphasis)

### Neutral Colors (Gray)
**Purpose**: Text, backgrounds, borders, general UI elements
- **50**: `#fafafa` - Very light gray (page backgrounds)
- **100**: `#f5f5f5` - Light gray (card backgrounds)
- **200**: `#e5e5e5` - Soft gray (borders, dividers)
- **300**: `#d4d4d4` - Medium light gray (disabled states)
- **400**: `#a3a3a3` - Medium gray (placeholder text)
- **500**: `#737373` - Gray (secondary text)
- **600**: `#525252` - Dark gray (body text)
- **700**: `#404040` - Darker gray (emphasis text)
- **800**: `#262626` - Very dark gray (headings)
- **900**: `#171717` - Darkest gray (strong emphasis)

## Semantic Color Classes

### Background Colors
```css
.bg-primary-light { @apply bg-primary-50; }
.bg-primary-medium { @apply bg-primary-500; }
.bg-primary-dark { @apply bg-primary-700; }
.bg-primary-gradient { @apply bg-gradient-to-r from-primary-600 to-primary-700; }

.bg-secondary-light { @apply bg-secondary-50; }
.bg-secondary-medium { @apply bg-secondary-500; }
.bg-secondary-dark { @apply bg-secondary-700; }
.bg-secondary-gradient { @apply bg-gradient-to-r from-secondary-600 to-secondary-700; }

.bg-success-light { @apply bg-success-50; }
.bg-success-medium { @apply bg-success-500; }
.bg-success-dark { @apply bg-success-700; }

.bg-warning-light { @apply bg-warning-50; }
.bg-warning-medium { @apply bg-warning-500; }
.bg-warning-dark { @apply bg-warning-700; }

.bg-error-light { @apply bg-error-50; }
.bg-error-medium { @apply bg-error-500; }
.bg-error-dark { @apply bg-error-700; }

.bg-info-light { @apply bg-info-50; }
.bg-info-medium { @apply bg-info-500; }
.bg-info-dark { @apply bg-info-700; }
```

### Text Colors
```css
.text-primary-light { @apply text-primary-600; }
.text-primary-medium { @apply text-primary-700; }
.text-primary-dark { @apply text-primary-800; }

.text-secondary-light { @apply text-secondary-600; }
.text-secondary-medium { @apply text-secondary-700; }
.text-secondary-dark { @apply text-secondary-800; }

.text-success-light { @apply text-success-600; }
.text-success-medium { @apply text-success-700; }
.text-success-dark { @apply text-success-800; }

.text-warning-light { @apply text-warning-600; }
.text-warning-medium { @apply text-warning-700; }
.text-warning-dark { @apply text-warning-800; }

.text-error-light { @apply text-error-600; }
.text-error-medium { @apply text-error-700; }
.text-error-dark { @apply text-error-800; }

.text-info-light { @apply text-info-600; }
.text-info-medium { @apply text-info-700; }
.text-info-dark { @apply text-info-800; }
```

### Border Colors
```css
.border-primary-light { @apply border-primary-200; }
.border-primary-medium { @apply border-primary-500; }
.border-primary-dark { @apply border-primary-700; }

.border-secondary-light { @apply border-secondary-200; }
.border-secondary-medium { @apply border-secondary-500; }
.border-secondary-dark { @apply border-secondary-700; }

.border-success-light { @apply border-success-200; }
.border-success-medium { @apply border-success-500; }
.border-success-dark { @apply border-success-700; }

.border-warning-light { @apply border-warning-200; }
.border-warning-medium { @apply border-warning-500; }
.border-warning-dark { @apply border-warning-700; }

.border-error-light { @apply border-error-200; }
.border-error-medium { @apply border-error-500; }
.border-error-dark { @apply border-error-700; }

.border-info-light { @apply border-info-200; }
.border-info-medium { @apply border-info-500; }
.border-info-dark { @apply border-info-700; }
```

### Interactive States
```css
.hover-primary { @apply hover:bg-primary-50 hover:text-primary-700; }
.hover-secondary { @apply hover:bg-secondary-50 hover:text-secondary-700; }
.hover-success { @apply hover:bg-success-50 hover:text-success-700; }
.hover-warning { @apply hover:bg-warning-50 hover:text-warning-700; }
.hover-error { @apply hover:bg-error-50 hover:text-error-700; }
.hover-info { @apply hover:bg-info-50 hover:text-info-700; }

.focus-primary { @apply focus:ring-2 focus:ring-primary-500 focus:ring-offset-2; }
.focus-secondary { @apply focus:ring-2 focus:ring-secondary-500 focus:ring-offset-2; }
.focus-success { @apply focus:ring-2 focus:ring-success-500 focus:ring-offset-2; }
.focus-warning { @apply focus:ring-2 focus:ring-warning-500 focus:ring-offset-2; }
.focus-error { @apply focus:ring-2 focus:ring-error-500 focus:ring-offset-2; }
.focus-info { @apply focus:ring-2 focus:ring-info-500 focus:ring-offset-2; }
```

## Usage Guidelines

### Primary Colors
- **Primary Blue (500-700)**: Use for main actions, links, and brand elements
- **Primary Light (50-200)**: Use for backgrounds, hover states, and subtle highlights
- **Primary Dark (800-900)**: Use for strong emphasis and headings

### Secondary Colors
- **Secondary Purple (500-700)**: Use for creative elements, spiritual content, and secondary actions
- **Secondary Light (50-200)**: Use for complementary backgrounds and subtle highlights
- **Secondary Dark (800-900)**: Use for emphasis in creative contexts

### Semantic Colors
- **Success**: Use for positive feedback, confirmations, and successful actions
- **Warning**: Use for caution messages, pending states, and attention needed
- **Error**: Use for error messages, destructive actions, and critical issues
- **Info**: Use for informational messages, neutral states, and general guidance

### Neutral Colors
- **Light Grays (50-200)**: Use for backgrounds, cards, and subtle UI elements
- **Medium Grays (300-500)**: Use for borders, dividers, and secondary text
- **Dark Grays (600-900)**: Use for body text, headings, and strong emphasis

## Accessibility Standards

### Contrast Ratios
All color combinations meet WCAG AA standards:
- **Normal text**: Minimum 4.5:1 contrast ratio
- **Large text**: Minimum 3:1 contrast ratio
- **UI components**: Minimum 3:1 contrast ratio

### Color Blindness Considerations
- Never rely solely on color to convey information
- Use additional visual cues (icons, patterns, text)
- Test color combinations for color blindness accessibility
- Ensure sufficient contrast for all color combinations

### Focus States
- All interactive elements have visible focus indicators
- Focus rings use semantic colors for consistency
- Focus states are clearly distinguishable from hover states

## Implementation Examples

### Buttons
```html
<!-- Primary button -->
<button class="bg-primary-600 hover:bg-primary-700 text-white px-4 py-2 rounded">
  Primary Action
</button>

<!-- Secondary button -->
<button class="bg-secondary-600 hover:bg-secondary-700 text-white px-4 py-2 rounded">
  Secondary Action
</button>

<!-- Success button -->
<button class="bg-success-600 hover:bg-success-700 text-white px-4 py-2 rounded">
  Success Action
</button>
```

### Cards
```html
<!-- Primary card -->
<div class="bg-white border border-gray-200 rounded-lg p-6 shadow-sm">
  <h3 class="text-gray-900 font-semibold">Card Title</h3>
  <p class="text-gray-600 mt-2">Card content goes here.</p>
</div>

<!-- Accent card -->
<div class="bg-primary-50 border border-primary-200 rounded-lg p-6">
  <h3 class="text-primary-800 font-semibold">Accent Card</h3>
  <p class="text-primary-700 mt-2">Accent content goes here.</p>
</div>
```

### Alerts
```html
<!-- Success alert -->
<div class="bg-success-50 border border-success-200 text-success-800 px-4 py-3 rounded">
  Success message goes here.
</div>

<!-- Warning alert -->
<div class="bg-warning-50 border border-warning-200 text-warning-800 px-4 py-3 rounded">
  Warning message goes here.
</div>

<!-- Error alert -->
<div class="bg-error-50 border border-error-200 text-error-800 px-4 py-3 rounded">
  Error message goes here.
</div>
```

## Best Practices

1. **Consistency**: Use the same color for the same purpose across the site
2. **Hierarchy**: Use color to establish visual hierarchy and importance
3. **Accessibility**: Always ensure sufficient contrast and color blindness accessibility
4. **Semantic Meaning**: Use semantic colors to convey meaning and context
5. **Subtlety**: Use light colors for backgrounds and strong colors for emphasis
6. **Testing**: Test color combinations across different devices and lighting conditions

## Maintenance

- Regularly review color usage for consistency
- Test accessibility compliance with automated tools
- Update color system documentation when changes are made
- Ensure all team members follow the color guidelines
- Monitor for any accessibility issues or user feedback 