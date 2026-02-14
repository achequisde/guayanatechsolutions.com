<script setup lang="ts">
import HomeProduct from '@/components/HomeProduct.vue';
import HomeService from '@/components/HomeService.vue';

const services = [
  { title: "Electrónica Industrial", text: "Reparación, mantenimiento y Suministros de equipos y tarjetas industriales, Instrumentación y control, sistema de riego." },
  { title: "Radiocomunicaciones", text: "Suministro de radios, programación, servicio técnico y accesorios." },
  { title: "Sistemas de seguridad, monitoreo y control", text: "Instalación de sistemas CCTV, control de acceso, alarmas y sensores, monitoreo a distancia." },
  { title: "Equipos médicos", text: "Equipos de Imagenología, Odontología, Oftalmología, Laboratorio, Cardiología, Radiología, Cámaras, equipos de belleza y Spa." },
  { title: "Diseño Electrónico y proyectos", text: "Diseño de circuitos y PCB para proyectos e investigaciones, simulaciones, suministro de componentes, programación." },
  { title: "Variadores de frecuencia", text: "Servicio técnico, instalación y suministro de Variadores de Frecuencia VDF, arrancadores suaves y ATS, switches de transferencia automática." },
];

const titles = [
  "innovation, solutions, and efficiency",
  "our services",
  "our products",
].map((e) => e.toUpperCase());

const products = [
  { title: "Tecnology", src: "https://placehold.co/600x400", alt: "Placeholder image" },
  { title: "Radios", src: "https://placehold.co/600x400", alt: "Placeholder image" },
  { title: "Variable-frequency drives", src: "https://placehold.co/600x400", alt: "Placeholder image" },
];

</script>

<template>
  <main>
    <section>
      <h1>{{ titles[0] }}</h1>
    </section>

    <section class="welcome-message">
      <div></div>
      <div>
        <h2>Guayana Tech Solutions</h2>
        <p>
          Somos una empresa especializada en Ingeniería Electrónica Industrial, con una amplia trayectoria en el área,
          te invitamos a conocer más sobre nosotros y lo que tenemos para ti.
        </p>
        <button class="btn btn--primary">Read more</button>
      </div>
    </section>

    <section class="services">
      <h2>{{ titles[1] }}</h2>

      <div class="services__container">
        <template v-for="service in services" :key="service.title">
          <HomeService v-bind="service" />
        </template>
      </div>
    </section>

    <section>
      <h2>
        Contamos con un amplio catálogo de
        Productos y Servicios para ti
      </h2>
      <button class="btn btn--primary">Contáctanos</button>
    </section>

    <section class="products">
      <h2>{{ titles[2] }}</h2>
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

<style>
.welcome-message {
  display: grid;

  grid-template-columns: 1fr 1fr;
}

.welcome-message>* {
  width: 50%;
}

.btn {
  padding: 10px 15px;
  font-weight: bold;

  border: 0px;

  border-radius: 25px;
}

.btn--primary {
  color: white;
  background: #FF8300;
}

.services__container {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
}
</style>
