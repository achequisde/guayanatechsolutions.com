<script setup lang="ts">
const props = defineProps<{
  title: string
  src: string
}>();

const image = `url('${props.src}')`;
</script>

<template>
  <div class="page-title__container">
    <h1 class="page-title title title--large text-center">{{ props.title }}</h1>
  </div>
</template>

<style scoped>
.page-title__container {
  background-image: v-bind(image);
  background-repeat: no-repeat;
  background-size: cover;
  background-position: center center;

  position: relative;
  z-index: 1;

  padding-top: 2rem;
}

.page-title__container::after {
  background: linear-gradient(180deg, #00DAC500 0%, #0FA098 60%);
  position: absolute;
  content: '';

  top: 0;
  bottom: 0;
  left: 0;
  right: 0;

  opacity: 0.5;
  z-index: -1;
}

h1 {
  text-transform: uppercase;
  padding: calc(2rem + 5vw);

  font-size: 60px;

  color: white;
}
</style>
