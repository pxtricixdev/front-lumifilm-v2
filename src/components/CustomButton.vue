<template>
  <button :type="type" :disabled="disabled" class="button">{{ label }}</button>
</template>

<script setup lang="ts">
defineProps<{
  label: string
  type: string
  disabled?: boolean
}>()
</script>

<style lang="scss" scoped>
@use '../assets/styles/variables' as *;
@use '../assets/styles/mixins' as *;

.button {
  @include semibold-text(16px);
  background-color: $blue-color;
  color: $white-color;
  border: none;
  border-radius: 15px;
  text-align: center;
  cursor: pointer;
}

.button:hover {
  opacity: 0.9;
  transition: ease-in 0.1s;
}
</style>
