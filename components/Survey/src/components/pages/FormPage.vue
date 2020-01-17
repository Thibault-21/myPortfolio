<template>
  <Page>
    <template #header>
      <h1>Survey Satisfaction Workplace</h1>
    </template>
      <Form v-if="step === 1" @onSubmitNext="next"/>
      <Form1 v-if="step === 2" @onSubmitNext="next" @onSubmitPrev="prev" />
      <Form2 v-if="step === 3" @onSubmitNext="next" @onSubmitPrev="prev"/>
      <Form3 v-if="step === 4" @onSubmit="FinalSubmit" @onSubmitPrev="prev"/> 
      <p v-if="step === 5">Thank you for participation <strong>{{sex}} {{Fname}} {{Lname}}</strong> !</p>
    <template #footer >
     <h3>by Thibault Decousus</h3>
    </template>
  </Page>
</template>

<script>
  import Page from "./Page";
  import Form from "../Form";
  import Form1 from "../Form1";
  import Form2 from "../Form2";
  import Form3 from "../Form3";

  export default {
    name: 'FormPage',
    components: {
      Page,
      Form,
      Form1,
      Form2,
      Form3,
    },
    data() {
      return {
        step: 1,
        name: "",
      }
    },
    methods: {
      next(Fname, Lname, sex) {
        if(Fname) this.Fname = Fname;
        if(Lname) this.Lname = Lname;
        if(sex) this.sex = sex; 

        this.step++;
      }, 
      prev(){
        this.step--;
      },
      FinalSubmit(){
        this.step++; 
      },
    }
  }
</script>

<style lang="scss" scoped>
 
</style>
