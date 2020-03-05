<template>
  <div class="container">
    <h1>{{ $t('greeting') }}</h1>
    <h1>Welcome to my portfolio</h1>

    <nuxt-link
      v-if="$i18n.locale !== 'en'"
      :to="switchLocalePath('en')"
    >
      English
    </nuxt-link>

    <nuxt-link
      v-if="$i18n.locale !== 'fr'"
      :to="switchLocalePath('fr')"
    >
      Español
    </nuxt-link>
    
  </div>
</template>

<script>
import Home from '../pages/home'
import Projects from '../pages/projects'
import Skills from '../pages/skills'
import About from '../pages/about'
import Contact from '../pages/contact'

export default {
  layout: 'default',
  components: {
    Home,
    Projects,
    Skills,
    About, 
    Contact
  }
}
</script>

<style scoped>

</style>
