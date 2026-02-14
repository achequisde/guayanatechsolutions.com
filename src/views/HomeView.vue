<script setup lang="ts">

const titles = [
  "innovation, solutions, and efficiency",
  "our services",
  "our products",
].map((e) => e.toUpperCase());

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

    <section>
      <h2>{{ titles[1] }}</h2>
    </section>

    <section>

    </section>

    <section>
      <h2>{{ titles[2] }}</h2>
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
</style>
