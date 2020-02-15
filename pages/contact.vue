<template>
  <div class="main">
      <FormContact></FormContact>
     <nuxt />
  </div>
</template>

<script>

import FormContact from '../pages/Contact/FormContact'

export default {
  layout: 'default',
  components: {
    FormContact
  }
}
</script>

<style scoped>

</style>
