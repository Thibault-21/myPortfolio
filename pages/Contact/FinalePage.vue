<template>
  <div class="main">
    <p><strong>{{name}}</strong></p>
    <nuxt />
  </div>
</template>

<script>
export default {
  name: 'FinalePage',
  props: {
    name: String
  },  
  // methods: {
  //   submitNext() {
  //     this.$emit('onSubmitNext', this.firstName, this.lastName, this.gender);
  //   }
  // }
}
</script>

<style>

</style>
