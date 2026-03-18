<template>
  <label class="polaris-checkbox-card" :class="{ 'polaris-checkbox-card--checked': modelValue }">
    <input
      type="checkbox"
      class="polaris-checkbox-card__input"
      :checked="modelValue"
      :disabled="disabled"
      @change="$emit('update:modelValue', $event?.target?.checked)"
    />
    <div class="polaris-checkbox-card__content">
      <span v-if="title" class="polaris-checkbox-card__title">{{ title }}</span>
      <span v-if="description" class="polaris-checkbox-card__desc">{{ description }}</span>
      <slot />
    </div>
  </label>
</template>

<script>
export default {
  name: 'PolarisCheckboxCard',
  props: {
    modelValue: { type: Boolean, default: false },
    title: { type: String, default: '' },
    description: { type: String, default: '' },
    disabled: { type: Boolean, default: false },
  },
  emits: ['update:modelValue'],
}
</script>

<style lang="scss" scoped>
@import 'polaris-weweb-styles';

.polaris-checkbox-card {
  @include polaris-tokens;
  display: flex;
  align-items: flex-start;
  gap: var(--p-space-300);
  padding: var(--p-space-300) var(--p-space-400);
  border: 1px solid var(--p-color-border);
  border-radius: var(--p-border-radius-200);
  background: var(--p-color-bg-surface);
  cursor: pointer;
  transition: all var(--p-motion-duration-150) var(--p-motion-ease);

  &:hover { background: var(--p-color-bg-surface-hover); }
  &--checked { border-color: var(--p-color-border-brand); background: var(--p-color-bg-surface-selected); }

  &__input {
    @include polaris-checkbox;
    margin-top: 2px;
  }

  &__content {
    display: flex;
    flex-direction: column;
    gap: var(--p-space-050);
    flex: 1;
  }

  &__title {
    font-family: var(--p-font-family-sans);
    font-size: var(--p-font-size-350);
    font-weight: var(--p-font-weight-medium);
    color: var(--p-color-text);
  }

  &__desc {
    font-family: var(--p-font-family-sans);
    font-size: var(--p-font-size-300);
    color: var(--p-color-text-secondary);
  }
}
</style>
