<template>
  <div class=main>
    <nav class="spacing">
      <nuxt-link class="routes" to="/">Home</nuxt-link>
      <nuxt-link class="routes" to="/projects">Projects</nuxt-link>
      <nuxt-link class="routes" to="/skills">Skills</nuxt-link>
      <nuxt-link class="routes" to="/about">About</nuxt-link>

      <a rel="noreferrer" 
         href="../CV_Thibault_Decousus_Vuejs.pdf" 
         download="static/CV Thibault Decousus Vue.js.pdf" 
         target="CV" 
         alt="CV">
         CV
      </a>

      <a rel="noreferrer" 
         href="https://github.com/Thibault-21" 
         target="_blank" 
         alt="github link">
         GitHub
      </a>

      <a rel="noreferrer" 
         href="https://www.linkedin.com/in/thibault-decousus/?locale=en_US" 
         target="_blank" 
         alt="linkedIn link">
         LinkedIn
      </a>

      <nuxt-link class="routes" to="/contact">Contact</nuxt-link>
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

<style scoped>

</style>
