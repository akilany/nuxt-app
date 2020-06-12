<template>
  <nav class="nav">
    <div class="container">
      <h3 class="brand">
        <nuxt-link to="/">Real Nuxt</nuxt-link>
      </h3>
      <ul class="links">
        <li><nuxt-link to="/show">List</nuxt-link></li>
        <li><nuxt-link to="/event/create">Create</nuxt-link></li>
      </ul>
    </div>
  </nav>
</template>

<script>
export default {}
</script>

<style>
.nav {
  display: flex;
  justify-content: center;
  padding: 1rem 0rem;
  background: rgb(41, 189, 209);
  color: #fff;
}

.nav .links {
  display: flex;
  justify-content: center;
  align-items: center;
  list-style: none;
}

.links li {
  padding-left: 1rem;
}

a {
  color: #fff;
  text-decoration: none;
}
</style>
