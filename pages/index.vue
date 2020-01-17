<template>
  <div class="container">
    <h1>Welcome to my portfolio</h1>
    <p @onThank="add"></p>
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
  }, 
  methods: {
    add(Fname, Lanme, sex){
      
    }
  }
}
</script>

<style lang="scss" scoped>

</style>
