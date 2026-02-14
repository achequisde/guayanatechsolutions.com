<script setup lang="ts">
const props = defineProps<{
  src: string
  alt: string
  title: string
}>();
</script>

<template>
  <img :src="props.src" :alt="props.alt">
  <h3>{{ props.title }}</h3>
</template>
