<script setup lang="ts">
import PageTitle from '@/components/PageTitle.vue';

</script>

<template>
  <main>
    <PageTitle title="about us" src="src/assets/closeup.jpg"></PageTitle>

    <div class="page-container">
      <section class="about-us">
        <h2 class="title text-center title--large">Our company</h2>

        <p>
          Con el propósito de impulsar el crecimiento sustentable en la industria nacional, sin depender de industrias
          extranjeras, nace la empresa Corporación Tecnológica de Guayana (CTG) en el 2015 desde la ciudad de Puerto
          Ordaz, estado Bolívar, Venezuela. Creada por Ingenieros electrónicos egresados de la Universidad Nacional
          Experimental Politécnica Antonio José de Sucre (UNEXPO), Vicerrectorado Puerto Ordaz. Desarrollada en un
          principio como una iniciativa ante la migración de empresas venezolanas que atienden sistemas de control
          industrial como PLC, variadores de frecuencia, arrancadores suaves y balanzas.
        </p>
        <p>
          Nuestros objetivos se basan en dar paso a acciones que involucren equipos de trabajo bien integrados,
          cohesivos, comprometidos, capacitados y formados que desempeñen sus funciones en pro de su entorno social y
          empresarial.
        </p>
        <p>
          En más de dos años nos formamos como una empresa destinada desde control de motores, hasta convertirnos en una
          empresa de íntegro desempeño en automatización industrial por PLC's, accionamientos automatizados por Servo
          Drives y Servo motores, variadores de frecuencia y Switch automáticos de frecuencia, desarrolladora de
          software para móviles y Páginas web, radiocomunicaciones móviles, servicios de calibración de balanzas
          dinámicas y estáticas.
        </p>
        <p>
          Contamos con especialistas en cada área, para maximizar la eficiencia y calidad a nuestro usuario final y
          lograr mantener una relación de calidad con nuestros clientes.
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
