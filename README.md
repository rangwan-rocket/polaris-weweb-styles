# Polaris WeWeb Styles

A Shopify Polaris-inspired design system for WeWeb custom components.

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
  @include polaris-tokens;  // Apply CSS variables
}

.my-button {
  @include polaris-button-primary;
}
</style>
```

## Theming / Custom Brand Colors

Edit `_variables.scss` before importing to change the brand color:

```scss
// In _variables.scss, change:
$brand-primary: #0070f3;  // Your brand color
```

Or override in your component:

```scss
.my-component {
  @include polaris-tokens;
  
  // Override brand color
  --p-color-bg-fill-brand: #0070f3;
  --p-color-text-brand: #0070f3;
  --p-color-border-brand: #0070f3;
}
```

## Documentation

- [Design Tokens Reference](docs/tokens.md)
- [Mixins Reference](docs/mixins.md)
- [Theming Guide](docs/theming.md)

## Available Mixins

### Tokens
- `@include polaris-tokens` - All CSS custom properties

### Buttons
- `@include polaris-button-primary` - Primary action
- `@include polaris-button-default` - Secondary action
- `@include polaris-button-plain` - Text-only button
- `@include polaris-button-critical` - Destructive action

### Cards
- `@include polaris-card` - Standard card
- `@include polaris-card-subdued` - Subdued card
- `@include polaris-card-section` - Card section

### Form Elements
- `@include polaris-input` - Text input
- `@include polaris-select` - Dropdown select
- `@include polaris-textarea` - Multi-line textarea
- `@include polaris-label` - Form label

### Badges & Banners
- `@include polaris-badge-info/success/warning/critical`
- `@include polaris-banner-info/success/warning/critical`

### Layout
- `@include polaris-inline($gap)` - Horizontal layout
- `@include polaris-block-stack($gap)` - Vertical layout

### Typography
- `@include polaris-text-heading-xl/lg/md/sm`
- `@include polaris-text-body`
- `@include polaris-text-body-subdued`

See [docs/mixins.md](docs/mixins.md) for complete reference.

## File Structure

```
polaris-weweb-styles/
├── index.scss          # Main entry point
├── _variables.scss     # Customizable brand colors
├── _tokens.scss        # Design tokens (CSS variables)
├── _mixins.scss        # Component mixins
├── docs/               # Documentation
└── examples/           # Visual examples
```

## Updating

After making changes:

```bash
git add .
git commit -m "Update styles"
git push
```

In your component projects:

```bash
npm update polaris-weweb-styles
```

## License

MIT
