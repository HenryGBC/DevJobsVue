<template>
  <section class="home-header">
    <header>
      <h1 class="home-title">
        Encuentra tu trabajo perfecto como desarrollador
      </h1>
      <p class="home-description">
        Dev Jobs es una plataforma donde puedes encontrar distintas vacantes
        como desarrollador, desde Frontend, Backends, Desarrolladores mobile y
        muchos mas
      </p>
    </header>
  </section>
</template>

<script>
export default {
  name: 'Navbar',
};
</script>

<style>
/* Header Styles */

.home-header {
  padding: 4rem 0;
}

.home-header .home-title {
  color: var(--green-primary);
  font-size: 3.5rem;
  line-height: 5rem;
  max-width: 50rem;
}
.home-header .home-description {
  color: var(--white-text-dark);
  font-size: 1.3rem;
  max-width: 41.5rem;
  line-height: 2rem;
  margin-top: 2rem;
}
</style>
