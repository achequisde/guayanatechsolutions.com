<script setup lang="ts">
import PageTitle from '@/components/PageTitle.vue';
import { nextTick, onMounted } from 'vue';

onMounted(() => {
  nextTick(() => window?.document?.body.scrollIntoView())
})
</script>

<template>
  <main>
    <PageTitle title="about us" src="src/assets/closeup.jpg"></PageTitle>

    <div class="page-container">
      <section class="about-us">
        <h2 class="title text-center title--large">Our company</h2>

        <p>
          With the goal of promoting sustenable growth within the national industry, without external dependencies,
          Guayana Tech Solutions is born in 2015. Founded by Electronic Engineers from the Universidad Nacional
          Experimental Politécnica Antonio José de Sucre (UNEXPO) Vicerrectorado Puerto Ordaz, it came as an answer to
          the migration of companies that tended to industrial control systems such as PLC, variable-frequency drives,
          soft starters, and scales.
        </p>
        <p>
          Our objectives are based on giving away to actions that well-integrated, cohesive, commited, and trained work
          teams that perform their functions in favor of our social and business environment.
        </p>
        <p>
          After more than five years in the business we have become a company with much expertise in industrial
          automatization via PLCs, automatic drives, variable-frequency drives, and automatic switchs, as well as
          software development for mobile and web pages, radiocommunications, and dynamic and static scales calibration.
        </p>
        <p>
          We have specialists for each area that we work with so as to improve the efficiency and quality of the work we
          do for our clients, making sure our relationship with them is rock solid.
        </p>
      </section>
      <div class="details">
        <section class="mission">
          <h2 class="title title--medium text-center">Mission</h2>
          <p>
            To be at the top in providing solutions via technology, striving to satisfy the needs our clients with
            expertise and commitment.
          </p>
        </section>
        <section class="vision">
          <h2 class="title title--medium text-center">Vision</h2>
          <p>
            To be an excellency-inspiring company recognized by its innovation and ingenuity in both solutions and
            services, promoting values that foster mutual trust between our team and our clients.
          </p>
        </section>
        <section class="values">
          <h2 class="title title--medium text-center">Our values</h2>
          <ul>
            <li>Teamwork: To build a slim multi-discipline work team apt in providing solutions.</li>
            <li>Cooperation: To synergize with our clients so as to provide the best answer in each situation.</li>
            <li>Innovation: To take into account new developments in technology, looking forwards for new and better
              services. </li>
            <li>Honesty: To follow truth, coherency, and justice, being fair and straight with our clients.</li>
            <li>Perseverance: To work tenaciously to achieve our goals.</li>
            <li>Service: To serve our clients with passion and kindness.</li>
          </ul>
        </section>
      </div>
    </div>
  </main>
</template>

<style scoped>
h2 {
  margin-block-end: 1rem;

  text-transform: uppercase;
}

div.page-container {
  margin-block-start: 6rem;
}

.about-us {
  margin-block-end: 6rem;
}

.about-us>p {
  margin-block-end: 2rem;
}

.page-container {
  max-width: 80vw;
  margin-inline: auto;
}

.details {
  display: flex;
  flex-direction: column;

  gap: 2rem;
  row-gap: 4rem;
}

.mission {
  grid-area: mission;
}

.vision {
  grid-area: vision;
}

.values {
  grid-area: values;
  margin-block-end: 5rem;
}

.values ul {
  list-style-type: circle;
}

.values li {
  padding-block: 0.5rem;
}

@media (min-width: 1024px) {
  .details {
    display: grid;

    grid-template-areas:
      'mission vision'
      'values values';
  }

  .page-container {
    max-width: 1024px;
  }
}
</style>
