<script setup lang="ts">
const props = defineProps<{
  src: string
  alt: string
  title: string
}>();
</script>

<template>
  <article>
    <img :src="props.src" :alt="props.alt">
    <h3 class="product-title title text-center">{{ props.title }}</h3>
  </article>
</template>

<style scoped>
article {
  text-align: center;
}

.product-title {
  margin-block-start: 2rem;
}

article>* {
  margin-block: 0.5rem;
  padding-inline: 0.5rem;
}
</style>
