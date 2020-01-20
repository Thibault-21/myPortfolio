<template>
  <div class="main">
      <FormContact v-if="step === 0" @onThank="thank"/>
      <!-- <FinalPage v-if="step === 1"/> -->
      <p v-if="step === 1">Thank you very much <strong>{{sex}} {{Fname}} {{Lname}} </strong><p/>
     <nuxt />
  </div>
     <!-- Thank you <strong>{{gender}} {{firstname}} {{lastName}}</strong> -->
     <!-- <FormContact v-if="step === 0" @onThank="finalStep"/> -->
     <!-- <FinalPage v-if="step === 1"/> -->
</template>

<script>
import FinalePage from '../pages/Contact/FinalePage' 
import FormContact from '../pages/Contact/FormContact'

export default {
  layout: 'default',
  components: {
    FinalePage, 
    FormContact
  },
  data(){
    return {
      step: 0,
      gender: "",
      firstName: "",
      lastName:"",
      email:"",
      phone:"",
      company:"",
      job:"",
      user: ""
    }
  },  
  methods: {
    thank(sex, Fname, Lname) {
        if(Fname) this.Fname = Fname;
        if(Lname) this.Lname = Lname;
        if(sex) this.sex = sex; 
        this.step++;
        this.user = "Thank you very much" + this.gender + this.firstName + this.lastName;
    }
  }
}
</script>

<style lang="scss" scoped>

</style>
