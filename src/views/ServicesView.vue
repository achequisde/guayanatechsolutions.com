<script setup lang="ts">
import PageTitle from '@/components/PageTitle.vue';
import router from '@/router';
import { nextTick, onMounted } from 'vue';

function* range(start: number, end: number) {
  let count = start;
  while (count < end) {
    yield count;
    count++;
  }
}

onMounted(() => {
  const section = router.currentRoute.value.hash.replace("#", "")
  if (section) {
    nextTick(() => window?.document?.getElementById(section)?.scrollIntoView())
  } else {
    nextTick(() => window?.document?.body.scrollIntoView())
  }
})


</script>

<template>
  <main>
    <PageTitle title="our services" src="src/assets/technician_working.jpg"></PageTitle>

    <div class="page-container">
      <section class="summary">
        <p>
          Our company, Guayana Tech Solutions, looks to help you grow, tapping into the needs of the national market,
          without depending on outside sources only; offering services of the highest quality in industrial control
          systems like PLC, variable-frequency drives, soft starters, and scales. Our team is known for our expertise in
          many areas and services. Among them:
        </p>
      </section>
      <section class="service-list">
        <article id="industrial-electronics">
          <h2 class="title title--small text-center">Industrial Electronics</h2>
          <p>
            We repair any kind of power electronics and I&C device, offering solutions for the industrial sector and
            other big businesses as well as for small and
            medium local companies. We sell, buy, and replace industrial machinery.
          </p>
        </article>
        <article id="radiocommunications">
          <h2 class="title title--small text-center">Radiocommunications</h2>
          <p>We perform maintenance and repairs of radiocommunication systems, HF-VHF-UHF, commercial, amateur, and
            marine. We sell equipment, antennas, and accessories of repeting VHF and UHF systems. We do installations
            and commissioning.
          </p>
        </article>
        <article id="security">
          <h2 class="title title--small text-center">Security, monitoring, and control systems</h2>
          <p>We offer custom irrigation systems for you and your business. We sell irrigation programmers, pop-up and
            impact sprinklers, solenoids and quick-coupling valves, rain guns. Best brands only.
          </p>
        </article>
        <article id="medical-equipment">
          <h2 class="title title--small text-center">Medical equipment</h2>
          <p>
            Maintenance and all-around repairs for medical equipment, as well as electrical and electronic inspections;
            system tests, adjustments
            and parts replacements, cleaning and oiling, among other support jobs besides the required training in the
            usage of the device.
          </p>
        </article>
        <article id="electronic-design">
          <h2 class="title title--small text-center">Electronic design and projects</h2>
          <p>
            We do custom circuit designs tailored to your needs. We do the whole design lifecycle, from
            conceptualization to assembly and commisioning, as well as communication for IoT, monitoring, or electronic
            control.
          </p>
        </article>
        <article id="drives">
          <h2 class="title title--small text-center">Variable-frequency drives</h2>
          <p>Maintenance for variable-frequency drives: lifecycle analysis, general reconditioning, remote asistance for
            quick spotting of problems, and preventive maintenance programs. Through nicely designed maintenance
            programs, we maximize the reliability of your drives, extending their lifespan.
          </p>
        </article>
      </section>
    </div>

    <section class="text-center contact-us">
      <div class="page-container contact-us__container">
        <h2 class="title">Need custom designs?</h2>
        <p>
          Contact and share your idea or need with us and with great confidentiality our team of engineers will be able
          to guide you thanks to our experience in designing electronic circuits for many applications.
        </p>
        <button class="btn btn--primary"><a href="mailto:admin@guayanatechsolutions.com">Contact us</a></button>
      </div>
    </section>

    <div class="page-container brands">
      <section class="brands__container">
        <h2 class="title title--medium text-center">SOME BRANDS WE WORK WITH</h2>

        <div class="brands-list">
          <div class="brand-image" v-for="n in range(12, 27)" :key="n">
            <img :src="`src/assets/brands/Marcas-${n}.jpg`" alt="">
          </div>
        </div>
      </section>
    </div>
  </main>
</template>

<style scoped>
article {
  margin-block: 2rem;
}

h2 {
  margin-block-end: 1rem;
}

.page-container {
  max-width: 1024px;
  margin-inline: auto;
  padding: 0 2rem;
}

.brands {
  margin-block: 5rem;
}

.summary {
  margin-block: 6rem;
}

.contact-us {
  background-image: url('src/assets/joven_inventora.jpg');
  background-attachment: fixed;
  background-position: center center;
  background-repeat: no-repeat;
  background-size: cover;
  color: white;

  position: relative;
  z-index: 1;

  margin-block: 2.5rem;
  font-size: 24px;
}

.contact-us h2 {
  font-size: 40px;
}

.contact-us button {
  font-size: inherit;
  padding: 0.75rem 2rem;
}

.contact-us::after {
  background: linear-gradient(180deg, #00DAC500 0%, #0FA098 0%);
  position: absolute;
  content: '';

  top: 0;
  bottom: 0;
  left: 0;
  right: 0;

  opacity: 0.5;
  z-index: -1;
}

.contact-us__container {
  padding: 2rem;
}

.contact-us__container>* {
  margin: 0.75rem;
}

.brands-list {
  display: grid;

  grid-template-columns: repeat(2, 1fr);
}

@media (min-width: 1024px) {
  .service-list {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 1rem;
  }

  .brands-list {
    grid-template-columns: repeat(3, 1fr);
  }
}
</style>
