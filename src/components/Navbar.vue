<template>
  <nav class="navbar">
    <div class="navbar-left">
      <img src="../assets/img/Heart.png" alt="Heart Logo" />
      <h3 class="navbar-name">DevJobs</h3>
    </div>
    <div class="navbar-right">
      <a href="#" class="navbar-url"> About </a>
      <button class="btn">Login</button>
    </div>
  </nav>
</template>

<script>
export default {
  name: 'Navbar',
};
</script>

<style>
.navbar {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 2rem 0;
}
.navbar .navbar-left {
  display: flex;
  align-items: center;
}
.navbar .navbar-left img {
  height: 20px;
  margin-right: 1rem;
  width: 20px;
}
.navbar .navbar-left .navbar-name {
  color: var(--white-text);
}
.navbar .navbar-right button {
  margin-left: 1rem;
}
</style>
