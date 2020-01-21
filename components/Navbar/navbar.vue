<template>
  <div class=main>
    <nav class="spacing">
      <nuxt-link class="routes" to="/home">Home</nuxt-link>
      <nuxt-link class="routes" to="/projects">Projects</nuxt-link>
      <nuxt-link class="routes" to="/skills">Skills</nuxt-link>
      <nuxt-link class="routes" to="/about">About</nuxt-link>
      <a href="https://www.dropbox.com/s/s02u5bwrn1h9x57/CV-Thibault%20Decousus.pdf?dl=0">CV</a>
      <a href="https://github.com/Thibault-21">GitHub</a>
      <a href="https://www.linkedin.com/in/thibault-decousus/?locale=en_US">LinkedIn</a>
      <nuxt-link class="routes" to="/contact">Contact</nuxt-link>
      <input type="search" placeholder="Research..."/>
      <img class="icon" :src="icon"/>
      <!-- ajouter les liens vers mon git hub et vers mon linkedIn -->
    </nav>
  </div>
</template>

<script>
export default {
  name: 'Navbar',
  data(){
    return {
      icon: "outline_language_white_18dp.png"
    }
  }
}
</script>

<style lang="scss" scoped>



</style>
