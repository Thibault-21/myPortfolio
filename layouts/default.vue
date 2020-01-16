<template>
 <div class="main">
    <nav class="spacing">
      <nuxt-link class="routes" to="/home">Home</nuxt-link>
      <nuxt-link class="routes" to="/project">Project</nuxt-link>
      <nuxt-link class="routes" to="/skills">Skills</nuxt-link>
      <nuxt-link class="routes" to="/about">About</nuxt-link>
      <nuxt-link class="routes" to="/contact">Contact</nuxt-link>
      <a href="">CV </a>
      <a href="">GitHub</a>
      <a href="LinkedIn">LinkedIn</a>
      <!-- ajouter les liens vers mon git hub et vers mon linkedIn -->
    </nav>
    <main>
    </main>
    <footer>
    </footer>
  </div>
</template>

<style lang="scss" scoped>

nav {
  background-color: rgb(27, 27, 50);
  padding: 20px;
  color: white;
}
 footer {
  background-color: rgb(162, 171, 221);
  color: white;
  padding: 25px;
  margin: 5px;
  border-radius: 5px;
}

.spacing{
  color: white;
  margin: 5px;
  padding: 25px;
  border-radius: 5px;
}
.routes, a {
  color: white;
  margin-right: 15px;
  text-decoration: none;
}

</style>
