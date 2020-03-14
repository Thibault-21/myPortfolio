<template>
  <div class="main">
      <Card></Card>
     <nuxt />
  </div>
</template>

<script>

import Card from '../pages/Contact/Card'

export default {
  layout: 'default',
  components: {
    Card
  }
}
</script>

<style scoped>

</style>
