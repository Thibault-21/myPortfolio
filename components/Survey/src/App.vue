<template>
  <div id="app">
    <FormPage />
  </div>
</template>

<script>
import FormPage from './components/pages/FormPage'

export default {
  name: 'app',
  components: {
    FormPage
  }
}
</script>

<style lang="scss" scoped>

#app {
  margin: 0px;
  font-family: Helvetica, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

</style>
