# Theming Guide

How to customize the design system for your brand.

## Quick Brand Color Change

### Option 1: Edit `_variables.scss`

```scss
$brand-primary: #0070f3;           // Your brand color
$brand-primary-hover: #0060d0;     // Darker for hover
$brand-primary-active: #0050b0;    // Even darker for active
```

### Option 2: Override in Component

```scss
.my-component {
  @include polaris-tokens;
  
  --p-color-bg-fill-brand: #0070f3;
  --p-color-text-brand: #0070f3;
  --p-color-border-brand: #0070f3;
}
```

## Pre-made Themes

### Blue
```scss
$brand-primary: #0070f3;
```

### Purple
```scss
$brand-primary: #7c3aed;
```

### Indigo
```scss
$brand-primary: #4f46e5;
```

### Teal
```scss
$brand-primary: #0d9488;
```

### Orange
```scss
$brand-primary: #ea580c;
```
