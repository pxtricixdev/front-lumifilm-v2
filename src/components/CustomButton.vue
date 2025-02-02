<template>
  <button :type="type" :disabled="disabled" :class="['button', size]">
    {{ label }}
  </button>
</template>

<script setup lang="ts">
defineProps<{
  label: string
  type: 'button' | 'submit' | 'reset'
  size: 'small' | 'medium' | 'large'
  disabled?: boolean
}>()
</script>

<style lang="scss" scoped>
@use '@/assets/styles/variables' as *;
@use '@/assets/styles/mixins' as *;

.button {
  background-color: $blue-color;
  color: $white-color;
  border: none;
  border-radius: 15px;
  text-align: center;
  cursor: pointer;

  &:hover {
    opacity: 0.9;
    transition: ease-in 0.1s;
  }

  &:disabled {
    background-color: #2b2b2b;
    cursor: not-allowed;
  }

  &.small {
    padding: 8px 25px;
    @include semibold-text(12px);
    height: 40px;
  }

  &.medium {
    padding: 12px 40px;
    @include semibold-text(16px);
    height: 45px;
  }

  &.large {
    padding: 14px 60px;
    @include semibold-text(18px);
    height: 50px;
  }
}
</style>
