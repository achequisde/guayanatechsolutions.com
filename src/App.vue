<script setup lang="ts">
const links = [
  { id: 1, src: "/", label: "Home", },
  { id: 2, src: "/about", label: "About", },
  { id: 3, src: "/services", label: "Services", },
];
</script>

<template>
  <header>
    <div class="desktop-only">
      <img src="@/assets/logo-completo-blanco.png" alt="">
    </div>
    <nav>
      <ul>
        <li v-for="link in links" :key="link.id">
          <RouterLink :to="link.src">{{ link.label }}</RouterLink>
        </li>
      </ul>
    </nav>
  </header>

  <main>
    <RouterView />
  </main>

  <footer class="text-center">
    <img src="@/assets/logo-ctg-blanco.png" alt="">
    <h2 class="title">GUAYANA TECH SOLUTIONS</h2>
    <nav>
      <ul>
        <li>Home</li>
        <li>About</li>
        <li>Services</li>
      </ul>
    </nav>
    <address>Av. 1, C.C. Ipeca, Urb. Unare II, Puerto Ordaz</address>
    <p>
      <a href="">admin@guayanatechsolutions.com</a>
    </p>
  </footer>
</template>

<style scoped>
header div {
  max-width: 200px;
}

header nav ul {
  display: flex;
}

header {
  display: flex;
  justify-content: center;
  column-gap: 10vw;
  align-items: center;
  position: absolute;
  background-color: transparent;
  z-index: 9999;
  left: 0;
  right: 0;

  font-weight: bold;
}

header :link {
  color: white;
}

header :visited {
  color: white;
}

header li {
  padding: 1.5rem;
}

footer {
  color: white;
  font-weight: bold;
  background-color: #0FA098;
  padding-block: 2rem;
}

footer h2 {
  font-size: 1.5rem;
}

footer img {
  max-width: 4rem;
  margin-bottom: 1rem;
}

footer>* {
  padding-block: 0.1rem;
}

footer li {
  padding: 0.5rem;
}

footer ul {
  display: flex;
  justify-content: center;
  column-gap: 0.5rem;
}

footer address,
footer p {
  padding-block: 0.5rem;
}
</style>
