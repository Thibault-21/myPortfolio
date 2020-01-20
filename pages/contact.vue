<template>
  <div class="main">
      <FormContact v-if="step === 0" @onThank="thank"/>
      <p v-if="step === 1">{{user}} <strong>{{sex}} {{Fname}} {{Lname}}</strong><p/>
     <nuxt />
  </div>
</template>

<script>

import FormContact from '../pages/Contact/FormContact'

export default {
  layout: 'default',
  components: {
    FormContact
  },
  data(){
    return {
      step: 0,
      user: ""
    }
  },  
  methods: {
    thank(sex, Fname, Lname) {
      if(sex) this.sex = sex; 
      if(Fname) this.Fname = Fname;
      if(Lname) this.Lname = Lname;
        
      this.step++;
      this.user = "Thank you very much" 
    }
  }
}
</script>

<style lang="scss" scoped>

</style>
