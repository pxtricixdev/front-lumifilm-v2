<template>
  <svg width="140" height="160" viewBox="0 0 300 320" xmlns="http://www.w3.org/2000/svg">
    <!-- Respaldo superior -->
    <path d="M60 50 Q150 0 240 50 V143 H60 Z" :fill="fill" :stroke="stroke" />

    <!-- Asiento -->
    <rect x="50" y="150" width="200" height="80" rx="20" ry="20" :fill="fill" :stroke="stroke" />

    <!-- Patas -->
    <rect x="70" y="230" width="40" height="50" rx="5" ry="5" :fill="fill" :stroke="stroke" />
    <rect x="190" y="230" width="40" height="50" rx="5" ry="5" :fill="fill" :stroke="stroke" />

    <!-- Brazos de la butaca -->
    <rect x="30" y="120" width="40" height="90" rx="20" ry="20" :fill="fill" :stroke="stroke" />
    <rect x="230" y="120" width="40" height="90" rx="20" ry="20" :fill="fill" :stroke="stroke" />
  </svg>
</template>

<script setup lang="ts">
defineProps<{
  stroke: string
  fill?: string
}>()
</script>
