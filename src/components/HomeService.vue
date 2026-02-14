<script setup lang="ts">
const props = defineProps<{
  title: string
  text: string
}>()
</script>

<template>
  <article>
    <h3>{{ props.title }}</h3>
    <p>{{ props.text }}</p>
    <button>Leer más >></button>
  </article>
</template>
