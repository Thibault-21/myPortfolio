<template>
   <form method="POST">
      <select class="firstLine" v-model="contactInfos.gender">
        <option disabled value="">Please Select Your Gender</option>
        <option value="Mrs">Mrs</option>
        <option value="Mr">Mr</option>
        <option value="Other">Other</option>
      </select>
      <input type="text" class="firstLine" v-model="contactInfos.firstName" placeholder="Your firstName">
      <input type="text" class="firstLine" v-model="contactInfos.lastName" placeholder="Your lastName">
      <input type="text" class="firstLine" v-model="contactInfos.email" placeholder="Your email">
      <input type="tel" class="secondLine" name="phone" pattern="[0-9]{2}-[0-9]{2}-[0-9]{2}-[0-9]{2}-[0-9]{2}" required v-model="contactInfos.phone" placeholder="Your phone">
      <input type="text" class="secondLine" v-model="contactInfos.company" placeholder="Your company">
      <input type="text" class="secondLine" v-model="contactInfos.job" placeholder="Your job">
      <button class="btn-s" type="submit" @click.prevent="thank">Submit</button>
     <nuxt />
    </form>
</template>

<script>
export default {
  name: 'FormContact', 
  data(){
    return {
      contactInfos: {
        gender: "",
        firstName: "",
        lastName:"",
        email:"",
        phone:"",
        company:"",
        job:"",
      }
    }
  }, 
  methods: {
    thank(){
      this.$emit('onThank',this.gender, this.lastName, this.firstName);
    }
  }
} 
</script>

<style lang="scss" scoped>
form {
    display: inline-grid;
    grid-template-columns: 150px 150px 150px;
    grid-template-rows: 75px 75px;
    grid-gap: 15px;
    padding: 20px;
}
.firstLine {
  // grid-column-start: 1;
  // grid-row-start: 1;
  border-radius: 5px;
  border: 1px solid rgb(27, 27, 50);
  height: 35px;
  padding: 5px;
  margin: 5px;
}
.secondLine {
  // grid-column-start: 1;
  // grid-row-start: 2;
  border-radius: 5px;
  border: 1px solid rgb(27, 27, 50);
  height: 35px;
  padding: 5px;
  margin: 5px;
}
// input {
//   grid-column-end: 4;
//   border-radius: 5px;
//   border: 1px solid rgb(27, 27, 50);
//   height: 35px;
//   padding: 5px;
//   margin: 5px;
// }
::placeholder {
  color: rgb(162, 171, 221);
}
// .select {
//   border-radius: 5px;
//   border: 1px solid rgb(27, 27, 50);
//   height: 45px;
//   padding: 5px;
//   margin: 5px;
// }
.btn-s {
  grid-column-start: 3;
  grid-row-start: 3;
  border-radius: 5px;
  background-color: rgb(27, 27, 50);
  color: white;
  border: 1px solid rgb(27, 27, 50);
  height: 45px;
  padding: 5px;
  margin: 5px;
}
</style>
