<template>
  <nav>
      <router-link class="hero" to="/">thevinelist</router-link>
      <div class="nav-links">
      <router-link class="nav-link" to="/#">Add Product</router-link>
      <router-link class="nav-link" to="/#">Sign up</router-link>
      <router-link class="nav-link" to="/#">Sign in</router-link>
      </div>
  </nav>
</template>

<script>
  export default {
    name: "NavBar",
  };
</script>

  <!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
nav {
  width: 100%;
  background-color: var(--vl-blue);
  font-size: 2rem;
  display: flex;
  color: white;
  height: 2.8em;
  align-items: center;
  justify-content: center;
}

.nav-link, .hero {
  color: white;
  text-decoration: none;
  font-size: 1.6rem;
}

.hero{
  font-size: 2rem;
}

.nav-links{
  display: flex;
  justify-content: space-between;
  position: absolute;
  right: 30px;
  width: 20%;
  white-space: nowrap;
}
</style>
