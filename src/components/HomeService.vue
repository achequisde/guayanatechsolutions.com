<script setup lang="ts">
const props = defineProps<{
  title: string
  text: string
}>()
</script>

<template>
  <article>
    <h3 class="title">{{ props.title }}</h3>
    <p>{{ props.text }}</p>
    <button>Leer más >></button>
  </article>
</template>

<style scoped>
article {
  padding: 1rem;
  text-align: center;

  display: flex;
  flex-direction: column;
  align-items: center;

  border: 1px solid black;
}

article>* {
  padding: 0.5em;
}

button {
  border: 0px;
  background: inherit;

  font-size: 1.0325rem;

  font-weight: bold;
}

h3 {
  font-size: 1.25rem;
}
</style>
