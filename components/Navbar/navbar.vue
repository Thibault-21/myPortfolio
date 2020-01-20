<template>
  <div class=main>
    <nav class="spacing">
      <nuxt-link class="routes" to="/home">Home</nuxt-link>
      <nuxt-link class="routes" to="/projects">Projects</nuxt-link>
      <nuxt-link class="routes" to="/skills">Skills</nuxt-link>
      <nuxt-link class="routes" to="/about">About</nuxt-link>
      <a href="file:///C:/Users/thibd/Downloads/CV-Thibault%20Decousus%20(1).pdf">CV</a>
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
