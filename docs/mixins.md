# Mixins Reference

All available SCSS mixins and how to use them.

## Tokens

### `polaris-tokens`

Applies all CSS custom properties to an element.

```scss
.my-component {
  @include polaris-tokens;
}
```

## Buttons

```scss
.btn-primary {
  @include polaris-button-primary;
}

.btn-secondary {
  @include polaris-button-default;
}

.btn-link {
  @include polaris-button-plain;
}

.btn-delete {
  @include polaris-button-critical;
}
```

## Cards

```scss
.card {
  @include polaris-card;
}

.card-nested {
  @include polaris-card-subdued;
}

.card-body {
  @include polaris-card-section;
}
```

## Form Elements

```scss
input {
  @include polaris-input;
}

select {
  @include polaris-select;
}

textarea {
  @include polaris-textarea;
}

label {
  @include polaris-label;
}
```

## Badges & Banners

```scss
.badge {
  @include polaris-badge-default;
}

.badge-success {
  @include polaris-badge-success;
}

.alert {
  @include polaris-banner-info;
}
```

## Layout

```scss
.row {
  @include polaris-inline;  // Horizontal
}

.stack {
  @include polaris-block-stack;  // Vertical
}
```

## Typography

```scss
.title {
  @include polaris-text-heading-lg;
}

.body {
  @include polaris-text-body;
}

.muted {
  @include polaris-text-body-subdued;
}
```
