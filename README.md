# Polaris WeWeb Styles

Shared Polaris design tokens and mixins for WeWeb custom components.

## Installation

In your WeWeb component project:

```bash
npm install github:rangwan-rocket/polaris-weweb-styles
```

## Usage

In your component's `<style>` block:

```scss
<style lang="scss" scoped>
@import 'polaris-weweb-styles';

.my-component {
  @include polaris-tokens;  // Apply all CSS variables
}

.my-button {
  @include polaris-button-primary;
}

.my-card {
  @include polaris-card;
}

.my-input {
  @include polaris-input;
}
</style>
```

## Available Mixins

### Tokens
- `polaris-tokens` - All Polaris CSS custom properties

### Buttons
- `polaris-button-primary`
- `polaris-button-default`
- `polaris-button-plain`
- `polaris-button-critical`

### Cards
- `polaris-card`
- `polaris-card-subdued`

### Form Elements
- `polaris-input`
- `polaris-select`
- `polaris-textarea`
- `polaris-label`

### Badges & Banners
- `polaris-badge-info/success/warning/critical`
- `polaris-banner-info/success/warning/critical`

## License

MIT
