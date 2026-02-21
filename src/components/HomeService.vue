<script setup lang="ts">
const props = defineProps<{
  title: string
  text: string
  src: string
  href: string
}>()
</script>

<template>
  <div>
    <article>
      <img :src="props.src" />
      <h3 class="title">{{ props.title }}</h3>
      <p>{{ props.text }}</p>
      <button>
        <RouterLink :to="`/services/#${href}`">Read more</RouterLink>
      </button>

    </article>
  </div>

</template>

<style scoped>
div {
  background-image: url("../assets/closeup.jpg");
  border-radius: 25px;
}

article {
  min-height: 100%;
  padding: 1rem 1rem 0 1rem;
  text-align: center;

  display: grid;

  grid-template-rows: repeat(4, 1fr);

  color: white;

  flex-direction: column;
  align-items: center;


  border-radius: 25px;
  background: linear-gradient(180deg, #00DAC500 0%, #0FA098 30%);
}

article>h3,
article>p {
  align-self: self-start;
}

button {
  cursor: pointer;
  position: relative;
  border: 0px;
  background: inherit;
  color: inherit;

  font-size: 1.0325rem;

  font-weight: bold;
}

button::after {
  content: '>>';
  position: absolute;
  margin-inline-start: 10px;
  color: orange;
  top: 2px;
}

h3 {
  font-size: 1.25rem;
}

img {
  max-width: 90px;
}
</style>
