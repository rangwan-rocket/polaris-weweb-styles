# Polaris WeWeb Styles

An SCSS design system for **WeWeb custom-coded components (Vue)** that adheres to **Shopify Polaris** design language.

## Purpose

WeWeb allows building applications with custom Vue components. When these components need to integrate with or resemble Shopify admin interfaces, they should follow the [Polaris Design System](https://shopify.dev/docs/api/app-home/polaris-web-components).

This library provides:
- **Design tokens** (CSS custom properties) matching Polaris specifications
- **SCSS mixins** for common UI patterns (buttons, cards, forms, etc.)
- **Theming support** for brand customization

> **Note:** This is a styling-only library. It does not include JavaScript behavior, Vue components, or interactivity. Use it to style your own Vue component markup.

## Installation

```bash
npm install github:rangwan-rocket/polaris-weweb-styles
```

## Quick Start

In your WeWeb component's `<style>` block:

```scss
<style lang="scss" scoped>
@import 'polaris-weweb-styles';

.my-component {
  @include polaris-tokens;  // Required: injects CSS custom properties
}

.my-button {
  @include polaris-button-primary;
}

.my-card {
  @include polaris-card;
}
</style>
```

## Theming

### Option 1: Edit `_variables.scss`

```scss
// In _variables.scss
$brand-primary: #0070f3;           // Your brand color
$brand-primary-hover: #0060d0;
$brand-primary-active: #0050b0;
$brand-primary-disabled: #99c4f7;
$brand-primary-light: #e8f4ff;
```

### Option 2: Override CSS Variables

```scss
.my-component {
  @include polaris-tokens;
  
  // Override brand colors
  --p-color-bg-fill-brand: #0070f3;
  --p-color-text-brand: #0070f3;
  --p-color-border-brand: #0070f3;
}
```

---

## Available Mixins

### Setup
| Mixin | Description |
|-------|-------------|
| `polaris-tokens` | **Required.** Injects all CSS custom properties. Apply to root element. |

### Actions
| Mixin | Description |
|-------|-------------|
| `polaris-button-primary` | Primary action button (brand color) |
| `polaris-button-default` | Secondary button (white background) |
| `polaris-button-plain` | Text-only button |
| `polaris-button-critical` | Destructive action (red) |
| `polaris-button-outline` | Dashed outline button |
| `polaris-button-slim` | Smaller button size |
| `polaris-button-full-width` | 100% width button |
| `polaris-button-icon-only` | Square icon button |
| `polaris-button-group` | Horizontal button layout |
| `polaris-button-group-segmented` | Connected button group |
| `polaris-link` | Styled anchor link |
| `polaris-link-monochrome` | Underlined link (no color) |

### Cards
| Mixin | Description |
|-------|-------------|
| `polaris-card` | Standard card container |
| `polaris-card-subdued` | Nested/subdued card (gray background) |
| `polaris-card-section` | Section with padding and dividers |
| `polaris-callout-card` | Card with image/illustration |

### Form Controls
| Mixin | Description |
|-------|-------------|
| `polaris-input` | Text input field |
| `polaris-select` | Dropdown select |
| `polaris-textarea` | Multi-line text area |
| `polaris-search-field` | Search input with icon |
| `polaris-label` | Form label |
| `polaris-help-text` | Helper/hint text |
| `polaris-error-text` | Error message |
| `polaris-checkbox` | Checkbox input |
| `polaris-checkbox-wrapper` | Checkbox + label container |
| `polaris-radio` | Radio button input |
| `polaris-radio-wrapper` | Radio + label container |
| `polaris-switch` | Toggle switch |
| `polaris-switch-wrapper` | Switch + label container |
| `polaris-date-field` | Date input with calendar icon |
| `polaris-datetime-field` | Date + time input |
| `polaris-color-field` | Color input with swatch |
| `polaris-drop-zone` | File upload drag-drop area |

### Date Picker
| Mixin | Description |
|-------|-------------|
| `polaris-date-picker` | Calendar container |
| `polaris-date-picker-header` | Month/year header |
| `polaris-date-picker-nav-button` | Previous/next buttons |
| `polaris-date-picker-weekdays` | Weekday labels row |
| `polaris-date-picker-days` | Days grid |
| `polaris-date-picker-day` | Day button |
| `polaris-date-picker-day-selected` | Selected day |
| `polaris-date-picker-day-today` | Current day |
| `polaris-date-picker-day-in-range` | Range selection |
| `polaris-time-picker` | Time input container |
| `polaris-time-input` | Hour/minute inputs |
| `polaris-datetime-picker` | Combined date + time |

### Color Picker
| Mixin | Description |
|-------|-------------|
| `polaris-color-picker` | Color picker container |
| `polaris-color-picker-main` | Saturation/brightness area |
| `polaris-color-picker-hue-slider` | Hue slider |
| `polaris-color-picker-alpha-slider` | Alpha/opacity slider |
| `polaris-color-picker-preview` | Color preview section |
| `polaris-color-picker-inputs` | RGBA input fields |
| `polaris-color-picker-swatches` | Preset color grid |
| `polaris-color-field-swatch` | Color swatch button |

### Feedback
| Mixin | Description |
|-------|-------------|
| `polaris-badge-*` | Status badges (default, info, success, warning, critical) |
| `polaris-banner-*` | Alert banners (info, success, warning, critical) |
| `polaris-spinner` | Loading spinner (20px) |
| `polaris-spinner-small` | Small spinner (16px) |
| `polaris-spinner-large` | Large spinner (44px) |
| `polaris-progress-bar` | Progress bar track |
| `polaris-progress-bar-fill` | Progress bar fill |
| `polaris-skeleton-text` | Loading placeholder text |
| `polaris-skeleton-display-text` | Loading placeholder heading |
| `polaris-skeleton-body-text` | Loading placeholder paragraph |
| `polaris-skeleton-thumbnail` | Loading placeholder image |

### Media
| Mixin | Description |
|-------|-------------|
| `polaris-avatar($size)` | User avatar (default 40px) |
| `polaris-avatar-small` | Small avatar (32px) |
| `polaris-avatar-large` | Large avatar (60px) |
| `polaris-avatar-initials` | Text initials styling |
| `polaris-thumbnail($size)` | Media thumbnail (default 60px) |
| `polaris-thumbnail-small` | Small thumbnail (40px) |
| `polaris-thumbnail-large` | Large thumbnail (80px) |
| `polaris-icon($size)` | Icon sizing (default 20px) |

### Structure
| Mixin | Description |
|-------|-------------|
| `polaris-divider` | Horizontal line separator |
| `polaris-grid($cols, $gap)` | CSS Grid layout |
| `polaris-grid-responsive` | Auto-fit responsive grid |
| `polaris-inline($gap)` | Horizontal flex layout |
| `polaris-block-stack($gap)` | Vertical flex layout |
| `polaris-table` | Data table |
| `polaris-table-header` | Table header cell |
| `polaris-table-cell` | Table data cell |
| `polaris-list` | Unstyled list |
| `polaris-list-bulleted` | Bulleted list |
| `polaris-list-numbered` | Numbered list |
| `polaris-page` | Page container |
| `polaris-empty-state` | Empty state container |

### Navigation
| Mixin | Description |
|-------|-------------|
| `polaris-tabs` | Tab list container |
| `polaris-tab` | Tab button |
| `polaris-tab-selected` | Active tab state |
| `polaris-pagination` | Pagination container |
| `polaris-pagination-button` | Pagination arrow button |

### Overlays
| Mixin | Description |
|-------|-------------|
| `polaris-tooltip-trigger` | CSS-only tooltip (use `data-tooltip` attr) |
| `polaris-popover` | Popover container |
| `polaris-modal-backdrop` | Modal overlay background |
| `polaris-modal` | Modal dialog |
| `polaris-modal-header` | Modal header |
| `polaris-modal-content` | Modal body |
| `polaris-modal-footer` | Modal footer |
| `polaris-action-list` | Dropdown action menu |
| `polaris-action-list-item` | Action menu item |

### Titles & Text
| Mixin | Description |
|-------|-------------|
| `polaris-text-heading-xl` | Extra large heading (28px) |
| `polaris-text-heading-lg` | Large heading (24px) |
| `polaris-text-heading-md` | Medium heading (20px) |
| `polaris-text-heading-sm` | Small heading (16px) |
| `polaris-text-body` | Body text (14px) |
| `polaris-text-body-subdued` | Muted body text |
| `polaris-chip` | Tag/keyword chip |
| `polaris-chip-clickable` | Interactive chip |
| `polaris-chip-removable` | Chip with remove button |

---

## Design Tokens

All tokens follow Polaris naming conventions. See [docs/tokens.md](docs/tokens.md) for the complete reference.

### Key Tokens

```scss
// Colors
--p-color-bg                    // Page background
--p-color-bg-surface            // Card/surface background
--p-color-bg-fill-brand         // Primary button fill
--p-color-text                  // Primary text
--p-color-text-secondary        // Muted text
--p-color-border                // Default borders

// Spacing (4px base)
--p-space-100                   // 4px
--p-space-200                   // 8px
--p-space-300                   // 12px
--p-space-400                   // 16px

// Typography
--p-font-size-350               // 14px (body)
--p-font-size-400               // 16px
--p-font-weight-medium          // 500
--p-font-weight-semibold        // 600

// Border Radius
--p-border-radius-200           // 8px (buttons, inputs)
--p-border-radius-300           // 12px (cards)
```

---

## File Structure

```
polaris-weweb-styles/
├── index.scss          # Main entry point
├── _variables.scss     # Customizable brand colors
├── _tokens.scss        # Design tokens (CSS variables)
├── _mixins.scss        # Component mixins
├── docs/               # Documentation
│   ├── mixins.md       # Mixin reference
│   ├── tokens.md       # Token reference
│   ├── theming.md      # Theming guide
│   └── gap-analysis.md # Coverage vs Polaris
└── examples/           # Visual examples
```

---

## Reference

- [Shopify Polaris Web Components](https://shopify.dev/docs/api/app-home/polaris-web-components)
- [Polaris Vue](https://ownego.github.io/polaris-vue/) (community Vue implementation)
- [Polaris Design Tokens](https://polaris.shopify.com/tokens)

## License

MIT
