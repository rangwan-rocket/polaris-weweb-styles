# Mixins Reference

SCSS mixins for Shopify Polaris-style components in WeWeb custom-coded Vue components.

---

## Setup

### `polaris-tokens`

**Required.** Injects all CSS custom properties onto an element. Must be included on a root/wrapper element.

```scss
.my-component {
  @include polaris-tokens;
}
```

---

## Buttons

### Variants

```scss
.btn-primary {
  @include polaris-button-primary;     // Brand color, primary actions
}

.btn-secondary {
  @include polaris-button-default;     // White background, secondary actions
}

.btn-plain {
  @include polaris-button-plain;       // Text-only, tertiary actions
}

.btn-critical {
  @include polaris-button-critical;    // Red, destructive actions
}

.btn-outline {
  @include polaris-button-outline;     // Dashed border, add actions
}
```

### Modifiers

```scss
.btn-small {
  @include polaris-button-primary;
  @include polaris-button-slim;        // Smaller padding
}

.btn-full {
  @include polaris-button-primary;
  @include polaris-button-full-width;  // 100% width
}

.btn-icon {
  @include polaris-button-default;
  @include polaris-button-icon-only;   // Square, icon-sized
}
```

### Button Group

```scss
.button-group {
  @include polaris-button-group;       // Spaced buttons
}

.button-group-segmented {
  @include polaris-button-group-segmented;  // Connected buttons
}
```

---

## Links

```scss
a {
  @include polaris-link;               // Brand color link
}

.link-mono {
  @include polaris-link-monochrome;    // Underlined, no color
}
```

---

## Cards

```scss
.card {
  @include polaris-card;
}

.card-subdued {
  @include polaris-card-subdued;       // Gray background
}

.card-section {
  @include polaris-card-section;       // Padding + dividers
}

.callout-card {
  @include polaris-callout-card;       // Card with illustration
}
```

---

## Form Controls

### Text Inputs

```scss
input[type="text"] {
  @include polaris-input;
}

textarea {
  @include polaris-textarea;
}

select {
  @include polaris-select;
}

.search-input {
  @include polaris-search-field;       // With search icon
}
```

### Labels & Help Text

```scss
label {
  @include polaris-label;
}

.hint {
  @include polaris-help-text;
}

.error {
  @include polaris-error-text;
}
```

### Checkbox

```scss
.checkbox-group {
  @include polaris-checkbox-wrapper;
}

input[type="checkbox"] {
  @include polaris-checkbox;
}
```

```html
<label class="checkbox-group">
  <input type="checkbox" />
  <span>Accept terms</span>
</label>
```

### Radio Button

```scss
.radio-group {
  @include polaris-radio-wrapper;
}

input[type="radio"] {
  @include polaris-radio;
}
```

```html
<label class="radio-group">
  <input type="radio" name="option" value="1" />
  <span>Option 1</span>
</label>
```

### Switch / Toggle

```scss
.switch-group {
  @include polaris-switch-wrapper;
}

input[type="checkbox"].switch {
  @include polaris-switch;
}
```

```html
<label class="switch-group">
  <input type="checkbox" class="switch" />
  <span>Enable feature</span>
</label>
```

---

## Date Picker

### Date Field

```scss
.date-input {
  @include polaris-date-field;          // With calendar icon
}

.datetime-input {
  @include polaris-datetime-field;      // Date + time
}
```

### Calendar

```scss
.date-picker {
  @include polaris-date-picker;
}

.picker-header {
  @include polaris-date-picker-header;
}

.picker-title {
  @include polaris-date-picker-title;
}

.picker-nav {
  @include polaris-date-picker-nav;
}

.nav-btn {
  @include polaris-date-picker-nav-button;
}

.weekdays {
  @include polaris-date-picker-weekdays;
}

.weekday {
  @include polaris-date-picker-weekday;
}

.days {
  @include polaris-date-picker-days;
}

.day {
  @include polaris-date-picker-day;
}

.day.selected {
  @include polaris-date-picker-day-selected;
}

.day.today {
  @include polaris-date-picker-day-today;
}

.day.outside {
  @include polaris-date-picker-day-outside;
}

.day.disabled {
  @include polaris-date-picker-day-disabled;
}

// For date range selection
.day.in-range {
  @include polaris-date-picker-day-in-range;
}

.day.range-start {
  @include polaris-date-picker-day-range-start;
}

.day.range-end {
  @include polaris-date-picker-day-range-end;
}
```

### Time Picker

```scss
.time-picker {
  @include polaris-time-picker;
}

.time-input {
  @include polaris-time-input;
}

.time-separator {
  @include polaris-time-separator;      // The ":" between hours/minutes
}

.period-toggle {
  @include polaris-time-period-toggle;  // AM/PM container
}

.period-btn {
  @include polaris-time-period-button;
}

.period-btn.active {
  // Active state is built into the mixin
}
```

### DateTime Picker

```scss
.datetime-picker {
  @include polaris-datetime-picker;
}

.datetime-divider {
  @include polaris-datetime-picker-divider;
}

.time-section {
  @include polaris-datetime-picker-time-section;
}

.time-label {
  @include polaris-datetime-picker-time-label;
}
```

---

## Color Picker

### Color Field

```scss
.color-field {
  @include polaris-color-field;
}

.color-input {
  @include polaris-color-field-input;
}

.color-swatch {
  @include polaris-color-field-swatch;
}

.swatch-color {
  @include polaris-color-field-swatch-color;
  // Set color via: style="background: #ff0000"
}
```

### Full Color Picker

```scss
.color-picker {
  @include polaris-color-picker;
}

.picker-main {
  @include polaris-color-picker-main;
  // Set hue via: style="background: linear-gradient(to right, white, hsl(120, 100%, 50%))"
}

.picker-dragger {
  @include polaris-color-picker-dragger;
  // Position via: style="left: 50%; top: 30%"
}

.sliders {
  @include polaris-color-picker-sliders;
}

.hue-slider {
  @include polaris-color-picker-hue-slider;
}

.alpha-slider {
  @include polaris-color-picker-alpha-slider;
}

.slider-thumb {
  @include polaris-color-picker-slider-thumb;
  // Position via: style="left: 50%"
}

.preview {
  @include polaris-color-picker-preview;
}

.preview-swatch {
  @include polaris-color-picker-preview-swatch;
}

.inputs {
  @include polaris-color-picker-inputs;
}

.input-group {
  @include polaris-color-picker-input-group;
}

.input-label {
  @include polaris-color-picker-input-label;
}

.rgba-input {
  @include polaris-color-picker-input;
}

// Preset color swatches
.swatches {
  @include polaris-color-picker-swatches;
}

.preset-swatch {
  @include polaris-color-picker-swatch;
}

.preset-swatch.selected {
  @include polaris-color-picker-swatch-selected;
}
```

---

## Drop Zone

### Basic Drop Zone

```scss
.drop-zone {
  @include polaris-drop-zone;
}

.drop-zone.active {
  @include polaris-drop-zone-active;    // Drag over state
}

.drop-zone.error {
  @include polaris-drop-zone-error;     // Invalid file
}

.drop-zone-icon {
  @include polaris-drop-zone-icon;
}

.drop-zone-text {
  @include polaris-drop-zone-text;
}

.drop-zone-hint {
  @include polaris-drop-zone-hint;
}
```

### With File List

```scss
.drop-zone-stack {
  @include polaris-drop-zone-stack;
}

.file-item {
  @include polaris-drop-zone-file;
}

.file-thumbnail {
  @include polaris-drop-zone-file-thumbnail;
}

.file-info {
  @include polaris-drop-zone-file-info;
}

.file-name {
  @include polaris-drop-zone-file-name;
}

.file-size {
  @include polaris-drop-zone-file-size;
}

.file-remove {
  @include polaris-drop-zone-file-remove;
}
```

---

## Badges

```scss
.badge {
  @include polaris-badge-default;      // Gray
}

.badge-info {
  @include polaris-badge-info;         // Blue
}

.badge-success {
  @include polaris-badge-success;      // Green
}

.badge-warning {
  @include polaris-badge-warning;      // Yellow
}

.badge-critical {
  @include polaris-badge-critical;     // Red
}
```

---

## Banners

```scss
.banner-info {
  @include polaris-banner-info;
}

.banner-success {
  @include polaris-banner-success;
}

.banner-warning {
  @include polaris-banner-warning;
}

.banner-critical {
  @include polaris-banner-critical;
}
```

---

## Chips / Tags

```scss
.chip {
  @include polaris-chip;
}

.chip-clickable {
  @include polaris-chip-clickable;     // Hover state
}

.chip-removable {
  @include polaris-chip-removable;     // With X button space
}
```

---

## Media

### Avatar

```scss
.avatar {
  @include polaris-avatar;             // 40px default
}

.avatar-sm {
  @include polaris-avatar-small;       // 32px
}

.avatar-lg {
  @include polaris-avatar-large;       // 60px
}

.avatar-initials {
  @include polaris-avatar;
  @include polaris-avatar-initials;    // Text styling
}
```

### Thumbnail

```scss
.thumbnail {
  @include polaris-thumbnail;          // 60px default
}

.thumbnail-sm {
  @include polaris-thumbnail-small;    // 40px
}

.thumbnail-lg {
  @include polaris-thumbnail-large;    // 80px
}
```

### Icon

```scss
.icon {
  @include polaris-icon;               // 20px default
}

.icon-sm {
  @include polaris-icon-small;         // 16px
}

.icon-lg {
  @include polaris-icon(24px);         // Custom size
}
```

---

## Feedback

### Spinner

```scss
.spinner {
  @include polaris-spinner;            // 20px
}

.spinner-sm {
  @include polaris-spinner-small;      // 16px
}

.spinner-lg {
  @include polaris-spinner-large;      // 44px
}
```

### Progress Bar

```scss
.progress {
  @include polaris-progress-bar;
}

.progress-fill {
  @include polaris-progress-bar-fill;
  width: 60%;  // Set via style or JS
}
```

```html
<div class="progress">
  <div class="progress-fill" style="width: 60%"></div>
</div>
```

### Skeleton Loading

```scss
.skeleton-heading {
  @include polaris-skeleton-display-text;
}

.skeleton-line {
  @include polaris-skeleton-body-text;
}

.skeleton-image {
  @include polaris-skeleton-thumbnail;
}
```

---

## Layout

### Stack

```scss
.row {
  @include polaris-inline;             // Horizontal, 8px gap
}

.row-tight {
  @include polaris-inline(var(--p-space-100));  // 4px gap
}

.stack {
  @include polaris-block-stack;        // Vertical, 16px gap
}

.stack-tight {
  @include polaris-block-stack(var(--p-space-200));  // 8px gap
}
```

### Grid

```scss
.grid {
  @include polaris-grid;               // 12 columns
}

.grid-responsive {
  @include polaris-grid-responsive;    // Auto-fit
}

.col-6 {
  @include polaris-grid-cell(6);       // Half width
}
```

### Divider

```scss
hr {
  @include polaris-divider;
}

hr.thick {
  @include polaris-divider-thick;
}
```

---

## Tables

```scss
table {
  @include polaris-table;
}

th {
  @include polaris-table-header;
}

td {
  @include polaris-table-cell;
}

tr {
  @include polaris-table-row-hover;
}

tr.selected {
  @include polaris-table-row-selected;
}

td.numeric {
  @include polaris-table-numeric;      // Right-aligned, tabular
}
```

---

## Lists

```scss
ul.plain {
  @include polaris-list;               // No bullets
}

ul.bullets {
  @include polaris-list-bulleted;
}

ol {
  @include polaris-list-numbered;
}
```

### Action List (Menu)

```scss
.action-list {
  @include polaris-action-list;
}

.action-item {
  @include polaris-action-list-item;
}

.action-item-destructive {
  @include polaris-action-list-item;
  @include polaris-action-list-item-destructive;
}
```

---

## Navigation

### Tabs

```scss
.tabs {
  @include polaris-tabs;
}

.tab {
  @include polaris-tab;
}

.tab.active {
  @include polaris-tab-selected;
}

.tab-panel {
  @include polaris-tab-panel;
}
```

### Pagination

```scss
.pagination {
  @include polaris-pagination;
}

.pagination-btn {
  @include polaris-pagination-button;
}
```

---

## Overlays

### Tooltip (CSS-only)

```scss
.has-tooltip {
  @include polaris-tooltip-trigger;
}
```

```html
<button class="has-tooltip" data-tooltip="Click to save">
  Save
</button>
```

### Popover

```scss
.popover {
  @include polaris-popover;
}

.popover-content {
  @include polaris-popover-content;
}

.popover-actions {
  @include polaris-popover-actions;
}
```

### Modal

```scss
.modal-backdrop {
  @include polaris-modal-backdrop;
}

.modal {
  @include polaris-modal;
}

.modal-header {
  @include polaris-modal-header;
}

.modal-content {
  @include polaris-modal-content;
}

.modal-footer {
  @include polaris-modal-footer;
}
```

---

## Page Layout

### Page

```scss
.page {
  @include polaris-page;
}

.page-header {
  @include polaris-page-header;
}

.page-title {
  @include polaris-page-title;
}

.page-actions {
  @include polaris-page-actions;
}
```

### Empty State

```scss
.empty-state {
  @include polaris-empty-state;
}

.empty-state-image {
  @include polaris-empty-state-image;
}

.empty-state-heading {
  @include polaris-empty-state-heading;
}

.empty-state-content {
  @include polaris-empty-state-content;
}
```

### Resource Item

```scss
.resource-item {
  @include polaris-resource-item;
}

.resource-item.selected {
  @include polaris-resource-item-selected;
}
```

### Description List

```scss
dl {
  @include polaris-description-list;
}

dt {
  @include polaris-description-term;
}

dd {
  @include polaris-description-details;
}
```

---

## Typography

```scss
h1 {
  @include polaris-text-heading-xl;    // 28px bold
}

h2 {
  @include polaris-text-heading-lg;    // 24px semibold
}

h3 {
  @include polaris-text-heading-md;    // 20px semibold
}

h4 {
  @include polaris-text-heading-sm;    // 16px semibold
}

p {
  @include polaris-text-body;          // 14px
}

.muted {
  @include polaris-text-body-subdued;  // Secondary color
}
```

---

## Complete Example

```vue
<template>
  <div class="product-form">
    <div class="card">
      <div class="card-header">
        <h3 class="title">Edit Product</h3>
        <span class="badge-success">Active</span>
      </div>
      
      <div class="card-body">
        <div class="form-group">
          <label class="label">Name</label>
          <input type="text" class="input" v-model="name">
        </div>
        
        <div class="form-group">
          <label class="label">Description</label>
          <textarea class="textarea" v-model="description"></textarea>
        </div>
        
        <label class="checkbox-group">
          <input type="checkbox" v-model="featured">
          <span>Featured product</span>
        </label>
      </div>
      
      <div class="card-footer">
        <button class="btn-secondary" @click="cancel">Cancel</button>
        <button class="btn-primary" @click="save">
          <span v-if="saving" class="spinner-sm"></span>
          <span v-else>Save</span>
        </button>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
@import 'polaris-weweb-styles';

.product-form {
  @include polaris-tokens;
}

.card {
  @include polaris-card;
}

.card-header {
  @include polaris-card-section;
  @include polaris-inline;
  justify-content: space-between;
}

.card-body {
  @include polaris-card-section;
  @include polaris-block-stack;
}

.card-footer {
  @include polaris-card-section;
  @include polaris-inline;
  justify-content: flex-end;
}

.title {
  @include polaris-text-heading-md;
}

.form-group {
  @include polaris-block-stack(var(--p-space-100));
}

.label {
  @include polaris-label;
}

.input {
  @include polaris-input;
}

.textarea {
  @include polaris-textarea;
}

.checkbox-group {
  @include polaris-checkbox-wrapper;
  
  input[type="checkbox"] {
    @include polaris-checkbox;
  }
}

.btn-primary {
  @include polaris-button-primary;
}

.btn-secondary {
  @include polaris-button-default;
}

.badge-success {
  @include polaris-badge-success;
}

.spinner-sm {
  @include polaris-spinner-small;
}
</style>
```
