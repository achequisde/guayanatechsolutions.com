<script setup lang="ts">
import HomeProduct from '@/components/HomeProduct.vue';
import HomeService from '@/components/HomeService.vue';
import PageTitle from '@/components/PageTitle.vue';

import { nextTick, onMounted } from 'vue';

onMounted(() => {
  nextTick(() => window?.document?.body.scrollIntoView())
})

const services = [
  {
    src: "src/assets/service_industry.svg",
    title: "Industrial Electronics",
    text: "Repairs, maintenance, and provision of industrial equipment and boards, I&C, irrigation systems, among others.",
    href: "industrial-electronics",
  },
  {
    src: "src/assets/service_radio.svg",
    title: "Radiocommunications",
    text: "Supply, programming, service, and accesories for radios.",
    href: "radiocommunications",
  },
  {
    src: "src/assets/service_camera.svg",
    title: "Security, monitoring, and control systems",
    text: "Installation of CCTV systems, access control, alarms, sensors, distance monitoring, among others.",
    href: "security",
  },
  {
    src: "src/assets/service_medic.svg",
    title: "Medical equipment",
    text: "Service for Imagenology, Odontology, Ophthalmology, Cardiology, and Radiograph equipment. Beauty and Spa appliances.",
    href: "medical-equipment",
  },
  {
    src: "src/assets/service_iot.svg",
    title: "Electronic design and projects",
    text: "Circuit and PCB design for projects and research. Simulation, programming, and supply of components",
    href: "electronic-design",
  },
  {
    src: "src/assets/service_varia.svg",
    title: "Variable-frequency drives",
    text: "Technical service, installation, and supply of Variable-frequency drives (VFD), soft starters, and automatic-transfer switches (ATS).",
    href: "drives",
  },
];

const titles = [
  "innovation, solutions, and efficiency",
  "our services",
  "some of our products",
].map((e) => e.toUpperCase());

const products = [
  { title: "Tecnology", src: "src/assets/Productos-24.jpg", alt: "Placeholder image" },
  { title: "Radios", src: "src/assets/Productos-11.jpg", alt: "Placeholder image" },
  { title: "Variable-frequency drives", src: "src/assets/4variadores-34.jpg", alt: "Placeholder image" },
];

</script>

<template>
  <main>
    <PageTitle :title="titles[0]!" src="src/assets/circuito.png"></PageTitle>

    <section class="welcome-message ">
      <div class="page-padding">
        <div class="welcome-message__image">
          <img width="400" height="400" src="@/assets/technician_working.jpg" alt="">
        </div>
        <div class="welcome-message__text text-center">
          <h2 class="title title--medium">Guayana Tech Solutions</h2>
          <p>
            We are a company focused on Electronic Engineering at the Industrial level, with a long history in the
            business. Discover more about us and what we can offer you.
          </p>
          <button class="btn btn--primary">
            <RouterLink to="/about">Read more</RouterLink>
          </button>
        </div>
      </div>
    </section>

    <section class="services page-padding">
      <h2 class="title title--large text-center">{{ titles[1] }}</h2>

      <div class="services__container">
        <template v-for="service in services" :key="service.title">
          <HomeService v-bind="service" />
        </template>
      </div>
    </section>

    <section class="contact-us text-center">
      <div class="contact-us__container page-padding">
        <h2 class="title--large">
          We got an ample list of Products and Services just for you
        </h2>
        <button class="btn btn--primary btn--large"><a href="mailto:admin@guayanatechsolutions.com">Contact
            us</a></button>
      </div>
    </section>

    <section class="products page-padding">
      <h2 class="title title--large text-center">{{ titles[2] }}</h2>
      <div class="products__container">
        <template v-for="product in products" :key="product.title">
          <HomeProduct v-bind="product" />
        </template>
      </div>
    </section>

    <section>
    </section>
  </main>
</template>

<style scoped>
.welcome-message {
  margin-top: 6rem;
}

.welcome-message>div {
  max-width: 90%;
  margin-inline: auto;
}

.welcome-message .title {
  margin-block-end: 0;
}

.welcome-message__image {
  margin-block-end: 2rem;
}

.welcome-message__text>* {
  margin-block: 0.5rem;
}

.page-padding {
  padding: 2rem;
  max-width: 80vw;
  margin-inline: auto;
}

.services__container {
  display: grid;

  gap: 1rem;
}

.title {
  margin-block-end: 2rem;
}

.contact-us {
  background-image: url('@/assets/joven_inventora.jpg');
  background-attachment: fixed;
  background-position: center center;
  background-repeat: no-repeat;
  background-size: cover;
  color: white;

  position: relative;
  z-index: 1;

  margin-block: 2.5rem;
}

.contact-us h2 {
  font-size: 60px;
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

.contact-us__container>* {
  margin: 0.75rem;
}

.products__container {
  display: grid;
  gap: 1rem;
}

.products {
  margin-block-end: 5rem;
}

@media (min-width: 1024px) {
  .page-padding {
    max-width: 1024px;
  }

  .welcome-message>div {
    display: flex;
    max-width: 70%;

    justify-content: center;
    align-items: center;

    column-gap: 2rem;
  }

  .welcome-message__image {
    flex: 1 1 200px;
  }

  .welcome-message__text {
    flex: 2 1 100px;
  }

  .services__container {
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
  }

  .contact-us__container {
    max-width: 50%;
  }

  .products__container {
    grid-template-columns: 1fr 1fr 1fr;
  }
}
</style>
