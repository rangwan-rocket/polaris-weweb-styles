# Design Tokens Reference

CSS custom properties based on [Shopify Polaris Design Tokens](https://polaris.shopify.com/tokens).

All tokens are injected via `@include polaris-tokens` and follow the `--p-` prefix convention.

---

## Colors

### Background Colors

| Token | Default | Usage |
|-------|---------|-------|
| `--p-color-bg` | `#f6f6f7` | Page/app background |
| `--p-color-bg-surface` | `#ffffff` | Card, panel, modal surfaces |
| `--p-color-bg-surface-secondary` | `#f6f6f7` | Subdued surfaces, nested cards |
| `--p-color-bg-surface-hover` | `#f1f2f3` | Surface hover state |
| `--p-color-bg-surface-active` | `#e7e8ea` | Surface active/pressed state |
| `--p-color-bg-surface-selected` | `#f2f7fe` | Selected row/item state |
| `--p-color-bg-surface-disabled` | `#fafafa` | Disabled surface |

### Fill Colors

| Token | Default | Usage |
|-------|---------|-------|
| `--p-color-bg-fill` | `#f1f1f1` | Default fill (badges) |
| `--p-color-bg-fill-hover` | `#e3e3e3` | Fill hover state |
| `--p-color-bg-fill-active` | `#d4d4d4` | Fill active state |
| `--p-color-bg-fill-transparent-hover` | `rgba(0,0,0,0.05)` | Transparent hover |
| `--p-color-bg-fill-transparent-active` | `rgba(0,0,0,0.08)` | Transparent active |

### Brand Colors

| Token | Default | Usage |
|-------|---------|-------|
| `--p-color-bg-fill-brand` | `#008060` | Primary buttons, accents |
| `--p-color-bg-fill-brand-hover` | `#006e52` | Brand hover state |
| `--p-color-bg-fill-brand-active` | `#005c45` | Brand active state |
| `--p-color-bg-fill-brand-disabled` | `#8ec5b5` | Disabled brand elements |

### Status Colors

| Token | Default | Usage |
|-------|---------|-------|
| `--p-color-bg-fill-critical` | `#e51c00` | Error/danger fill |
| `--p-color-bg-fill-critical-secondary` | `#fee9e8` | Error background |
| `--p-color-bg-fill-success` | `#008060` | Success fill |
| `--p-color-bg-fill-success-secondary` | `#cdfee1` | Success background |
| `--p-color-bg-fill-warning` | `#ffb800` | Warning fill |
| `--p-color-bg-fill-warning-secondary` | `#fff5d6` | Warning background |
| `--p-color-bg-fill-info` | `#0070f3` | Info fill |
| `--p-color-bg-fill-info-secondary` | `#e8f4ff` | Info background |

### Text Colors

| Token | Default | Usage |
|-------|---------|-------|
| `--p-color-text` | `#202223` | Primary text |
| `--p-color-text-secondary` | `#6d7175` | Secondary/muted text |
| `--p-color-text-disabled` | `#8c9196` | Disabled text |
| `--p-color-text-on-color` | `#ffffff` | Text on colored backgrounds |
| `--p-color-text-brand` | `#008060` | Brand-colored text, links |
| `--p-color-text-critical` | `#e51c00` | Error text |
| `--p-color-text-success` | `#008060` | Success text |
| `--p-color-text-warning` | `#8a6116` | Warning text |
| `--p-color-text-info` | `#0070f3` | Info text |

### Border Colors

| Token | Default | Usage |
|-------|---------|-------|
| `--p-color-border` | `#c9cccf` | Default borders |
| `--p-color-border-hover` | `#8c9196` | Border hover state |
| `--p-color-border-disabled` | `#d9dbdd` | Disabled borders |
| `--p-color-border-brand` | `#008060` | Brand accent borders |
| `--p-color-border-critical` | `#e51c00` | Error borders |
| `--p-color-border-success` | `#008060` | Success borders |
| `--p-color-border-warning` | `#ffb800` | Warning borders |
| `--p-color-border-info` | `#0070f3` | Info borders |

### Icon Colors

| Token | Default | Usage |
|-------|---------|-------|
| `--p-color-icon` | `#5c5f62` | Default icon color |
| `--p-color-icon-hover` | `#1a1c1d` | Icon hover state |
| `--p-color-icon-disabled` | `#babfc4` | Disabled icons |
| `--p-color-icon-critical` | `#e51c00` | Error icons |
| `--p-color-icon-success` | `#008060` | Success icons |
| `--p-color-icon-warning` | `#ffb800` | Warning icons |
| `--p-color-icon-info` | `#0070f3` | Info icons |

### Focus

| Token | Default | Usage |
|-------|---------|-------|
| `--p-color-focus-ring` | `#005bd3` | Focus outline color |

---

## Spacing

Based on a **4px grid system**. Use these for consistent padding, margins, and gaps.

| Token | Value | Common Use |
|-------|-------|------------|
| `--p-space-0` | `0` | Reset spacing |
| `--p-space-025` | `1px` | Hairline spacing |
| `--p-space-050` | `2px` | Tight spacing |
| `--p-space-100` | `4px` | Extra small (icon gaps) |
| `--p-space-150` | `6px` | Small |
| `--p-space-200` | `8px` | Default small (button padding) |
| `--p-space-300` | `12px` | Medium (banner padding) |
| `--p-space-400` | `16px` | Default (card padding) |
| `--p-space-500` | `20px` | Large |
| `--p-space-600` | `24px` | Extra large |
| `--p-space-800` | `32px` | Section spacing |
| `--p-space-1000` | `40px` | Page sections |
| `--p-space-1200` | `48px` | Major sections |

### Usage Examples

```scss
// Button padding
padding: var(--p-space-150) var(--p-space-300);

// Card padding
padding: var(--p-space-400);

// Stack gap
gap: var(--p-space-200);

// Section margin
margin-bottom: var(--p-space-600);
```

---

## Typography

### Font Families

| Token | Value |
|-------|-------|
| `--p-font-family-sans` | System sans-serif stack |
| `--p-font-family-mono` | System monospace stack |

### Font Sizes

| Token | Value | Usage |
|-------|-------|-------|
| `--p-font-size-275` | `11px` | Extra small (captions) |
| `--p-font-size-300` | `12px` | Small (badges, help text) |
| `--p-font-size-325` | `13px` | Small body |
| `--p-font-size-350` | `14px` | **Default body text** |
| `--p-font-size-400` | `16px` | Large body, small heading |
| `--p-font-size-500` | `20px` | Medium heading |
| `--p-font-size-600` | `24px` | Large heading |
| `--p-font-size-700` | `28px` | Extra large heading |

### Line Heights

| Token | Value | Pairs with |
|-------|-------|------------|
| `--p-font-line-height-300` | `16px` | font-size-275, 300 |
| `--p-font-line-height-400` | `20px` | font-size-325, 350 |
| `--p-font-line-height-500` | `24px` | font-size-400 |
| `--p-font-line-height-600` | `28px` | font-size-500, 600 |
| `--p-font-line-height-700` | `32px` | font-size-700 |

### Font Weights

| Token | Value | Usage |
|-------|-------|-------|
| `--p-font-weight-regular` | `400` | Body text |
| `--p-font-weight-medium` | `500` | Labels, buttons |
| `--p-font-weight-semibold` | `600` | Headings |
| `--p-font-weight-bold` | `700` | Emphasis, large headings |

---

## Border Radius

| Token | Value | Usage |
|-------|-------|-------|
| `--p-border-radius-0` | `0` | No radius |
| `--p-border-radius-050` | `2px` | Subtle rounding |
| `--p-border-radius-100` | `4px` | Small elements |
| `--p-border-radius-150` | `6px` | Medium elements |
| `--p-border-radius-200` | `8px` | **Buttons, inputs** |
| `--p-border-radius-300` | `12px` | **Cards** |
| `--p-border-radius-400` | `16px` | Large cards |
| `--p-border-radius-full` | `9999px` | Pills, avatars |

---

## Shadows

| Token | Usage |
|-------|-------|
| `--p-shadow-0` | No shadow |
| `--p-shadow-100` | Subtle elevation |
| `--p-shadow-200` | Light elevation |
| `--p-shadow-card` | **Card default** |
| `--p-shadow-card-hover` | Card hover state |
| `--p-shadow-button` | Default button shadow |
| `--p-shadow-button-primary` | Primary button shadow |
| `--p-shadow-inset-100` | Input inner shadow |
| `--p-shadow-popover` | Dropdown/popover shadow |

---

## Motion

| Token | Value | Usage |
|-------|-------|-------|
| `--p-motion-duration-0` | `0ms` | No animation |
| `--p-motion-duration-50` | `50ms` | Micro interactions |
| `--p-motion-duration-100` | `100ms` | Fast transitions |
| `--p-motion-duration-150` | `150ms` | **Default transitions** |
| `--p-motion-duration-200` | `200ms` | Medium transitions |
| `--p-motion-duration-300` | `300ms` | Slow transitions |
| `--p-motion-ease` | `cubic-bezier(...)` | Standard easing |
| `--p-motion-ease-in` | `cubic-bezier(...)` | Entrance easing |
| `--p-motion-ease-out` | `cubic-bezier(...)` | Exit easing |

### Usage Example

```scss
.element {
  transition: background var(--p-motion-duration-150) var(--p-motion-ease),
              box-shadow var(--p-motion-duration-150) var(--p-motion-ease);
}
```

---

## Accessibility Notes

### Color Contrast

All text/background combinations meet WCAG 2.1 AA requirements:
- `--p-color-text` on `--p-color-bg-surface` → **12.6:1** ✓
- `--p-color-text-on-color` on `--p-color-bg-fill-brand` → **4.5:1** ✓
- `--p-color-text-secondary` on `--p-color-bg-surface` → **4.8:1** ✓

### Focus States

Always include visible focus indicators:

```scss
&:focus-visible {
  outline: 2px solid var(--p-color-focus-ring);
  outline-offset: 2px;
}
```

### Motion Preferences

Respect user preferences for reduced motion:

```scss
@media (prefers-reduced-motion: reduce) {
  * {
    transition-duration: 0.01ms !important;
  }
}
```
