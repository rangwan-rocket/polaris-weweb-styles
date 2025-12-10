# Theming Guide

Customize the Polaris design system for your brand while maintaining visual consistency.

---

## Quick Start

### Option 1: Edit `_variables.scss` (Recommended)

Before importing the library, modify the SCSS variables:

```scss
// In _variables.scss
$brand-primary: #0070f3;           // Your brand color
$brand-primary-hover: #0060d0;     // 10-15% darker
$brand-primary-active: #0050b0;    // 20-25% darker
$brand-primary-disabled: #99c4f7;  // 50% lighter
$brand-primary-light: #e8f4ff;     // 90% lighter (backgrounds)
```

### Option 2: CSS Variable Override

Override tokens directly in your component:

```scss
.my-component {
  @include polaris-tokens;
  
  // Override brand colors
  --p-color-bg-fill-brand: #0070f3;
  --p-color-bg-fill-brand-hover: #0060d0;
  --p-color-bg-fill-brand-active: #0050b0;
  --p-color-text-brand: #0070f3;
  --p-color-border-brand: #0070f3;
}
```

---

## Pre-made Themes

Copy any theme into your `_variables.scss`:

### Shopify Green (Default)
```scss
$brand-primary: #008060;
$brand-primary-hover: #006e52;
$brand-primary-active: #005c45;
$brand-primary-disabled: #8ec5b5;
$brand-primary-light: #cdfee1;
```

### Blue (Corporate)
```scss
$brand-primary: #0070f3;
$brand-primary-hover: #0060d0;
$brand-primary-active: #0050b0;
$brand-primary-disabled: #99c4f7;
$brand-primary-light: #e8f4ff;
```

### Purple (Creative)
```scss
$brand-primary: #7c3aed;
$brand-primary-hover: #6d28d9;
$brand-primary-active: #5b21b6;
$brand-primary-disabled: #c4b5fd;
$brand-primary-light: #ede9fe;
```

### Indigo (Tech)
```scss
$brand-primary: #4f46e5;
$brand-primary-hover: #4338ca;
$brand-primary-active: #3730a3;
$brand-primary-disabled: #a5b4fc;
$brand-primary-light: #e0e7ff;
```

### Teal (Fresh)
```scss
$brand-primary: #0d9488;
$brand-primary-hover: #0f766e;
$brand-primary-active: #115e59;
$brand-primary-disabled: #5eead4;
$brand-primary-light: #ccfbf1;
```

### Orange (Bold)
```scss
$brand-primary: #ea580c;
$brand-primary-hover: #c2410c;
$brand-primary-active: #9a3412;
$brand-primary-disabled: #fdba74;
$brand-primary-light: #ffedd5;
```

### Rose (Warm)
```scss
$brand-primary: #e11d48;
$brand-primary-hover: #be123c;
$brand-primary-active: #9f1239;
$brand-primary-disabled: #fda4af;
$brand-primary-light: #ffe4e6;
```

### Neutral (Minimal)
```scss
$brand-primary: #475569;
$brand-primary-hover: #334155;
$brand-primary-active: #1e293b;
$brand-primary-disabled: #94a3b8;
$brand-primary-light: #f1f5f9;
```

---

## Creating Custom Themes

### Step 1: Choose Base Color

Start with your brand's primary color (hex value).

### Step 2: Generate Color Variants

| Variant | Rule | Example (Blue #0070f3) |
|---------|------|------------------------|
| Hover | 10-15% darker | `#0060d0` |
| Active | 20-25% darker | `#0050b0` |
| Disabled | 40-50% lighter, desaturated | `#99c4f7` |
| Light | 85-95% lighter | `#e8f4ff` |

**Tools:**
- [Coolors](https://coolors.co/) — Generate palettes
- [Tint & Shade Generator](https://maketintsandshades.com/) — Create variations
- [Contrast Checker](https://webaim.org/resources/contrastchecker/) — Verify accessibility

### Step 3: Test Contrast

Ensure readability:

| Combination | Minimum Ratio |
|-------------|---------------|
| White text on brand fill | 4.5:1 (AA) |
| Brand text on white background | 4.5:1 (AA) |
| Brand text on light brand background | 3:1 (AA Large) |

> **Tip:** Dark brand colors (like Shopify green `#008060`) work well. Very light or saturated colors may fail contrast requirements for button text.

---

## Advanced Theming

### Full Token Override

For complete control, override all relevant tokens:

```scss
.my-component {
  @include polaris-tokens;
  
  // Surface colors
  --p-color-bg: #f8fafc;
  --p-color-bg-surface: #ffffff;
  --p-color-bg-surface-secondary: #f1f5f9;
  
  // Brand colors
  --p-color-bg-fill-brand: #0070f3;
  --p-color-bg-fill-brand-hover: #0060d0;
  --p-color-bg-fill-brand-active: #0050b0;
  --p-color-text-brand: #0070f3;
  --p-color-border-brand: #0070f3;
  
  // Text colors
  --p-color-text: #0f172a;
  --p-color-text-secondary: #64748b;
  
  // Border colors
  --p-color-border: #e2e8f0;
  --p-color-border-hover: #cbd5e1;
  
  // Focus
  --p-color-focus-ring: #0070f3;
}
```

### Component-Specific Overrides

Override tokens for specific contexts:

```scss
// Danger zone section
.danger-zone {
  --p-color-bg-fill-brand: var(--p-color-bg-fill-critical);
  --p-color-bg-fill-brand-hover: #c41200;
  --p-color-text-brand: var(--p-color-text-critical);
}

// Inside danger zone, primary buttons become red
.danger-zone .btn-primary {
  @include polaris-button-primary;
}
```

---

## Dark Mode (Experimental)

The token architecture supports dark mode via CSS variable overrides:

```scss
.my-component--dark {
  // Surfaces
  --p-color-bg: #0f172a;
  --p-color-bg-surface: #1e293b;
  --p-color-bg-surface-secondary: #334155;
  --p-color-bg-surface-hover: #475569;
  
  // Text
  --p-color-text: #f8fafc;
  --p-color-text-secondary: #94a3b8;
  
  // Borders
  --p-color-border: #475569;
  --p-color-border-hover: #64748b;
  
  // Icons
  --p-color-icon: #94a3b8;
  --p-color-icon-hover: #f8fafc;
  
  // Shadows (reduce intensity in dark mode)
  --p-shadow-card: 0 0 0 1px rgba(255, 255, 255, 0.1);
  --p-shadow-inset-100: inset 0 1px 1px rgba(0, 0, 0, 0.3);
}
```

### Auto Dark Mode

```scss
@media (prefers-color-scheme: dark) {
  .my-component {
    // Dark mode tokens...
  }
}
```

> **Note:** Full dark mode support requires testing all component states and may need additional token additions.

---

## WeWeb Integration

### Per-Component Theming

Each WeWeb component can have its own theme:

```vue
<template>
  <div class="component-root">
    <!-- Component content -->
  </div>
</template>

<style lang="scss" scoped>
@import 'polaris-weweb-styles';

.component-root {
  @include polaris-tokens;
  
  // This component uses blue theme
  --p-color-bg-fill-brand: #0070f3;
  --p-color-text-brand: #0070f3;
}
</style>
```

### Shared Theme via Props

Pass theme as a prop and apply conditionally:

```vue
<template>
  <div :class="['component-root', `theme-${theme}`]">
    <!-- Component content -->
  </div>
</template>

<script>
export default {
  props: {
    theme: {
      type: String,
      default: 'default',
      validator: v => ['default', 'blue', 'purple'].includes(v)
    }
  }
}
</script>

<style lang="scss" scoped>
@import 'polaris-weweb-styles';

.component-root {
  @include polaris-tokens;
}

.theme-blue {
  --p-color-bg-fill-brand: #0070f3;
  --p-color-text-brand: #0070f3;
}

.theme-purple {
  --p-color-bg-fill-brand: #7c3aed;
  --p-color-text-brand: #7c3aed;
}
</style>
```
