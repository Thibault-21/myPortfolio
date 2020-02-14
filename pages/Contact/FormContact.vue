<template>
  <form action="" method="POST" class="main">
   <div class="user">
     <label v-if="step === 0" class="firstLine">
      <select v-model="user.gender">
       <option disabled value="">Please Select Your Gender</option>
       <option value="Mrs">Mrs</option>
       <option value="Mr">Mr</option>
       <option value="Other">Other</option>
      </select>
      <button @click.prevent="next" class="next">Next</button>
     </label>
     <label v-else-if="step === 1">
      <button @click.prevent="previous" class="previous">Back</button>
      <input type="text" v-model="firstName" placeholder="Your firstName">
      <input type="text" v-model="lastName" placeholder="Your lastName">
      <button @click.prevent="next" class="next">Next</button>
     </label>
     <label v-else-if="step === 2">
      <button @click.prevent="previous" class="previous">Back</button>
      <input type="text" v-model="company" placeholder="Your company">
      <input type="text" v-model="job" placeholder="Your job">
      <button @click.prevent="next" class="next">Next</button>
     </label>
     <label v-else-if="step === 3">
      <button @click.prevent="previous" class="previous">Back</button>
      <input type="text" v-model="email" placeholder="Your email">
      <input type="tel" name="phone" pattern="[0-9]{2}-[0-9]{2}-[0-9]{2}-[0-9]{2}-[0-9]{2}" required v-model="phone" placeholder="Your phone">
      <button class="btn-s" type="submit" @click="submit">Submit</button>
     </label>
    </div>
  <nuxt />
 </form>
</template>

<script>
export default {
  name: 'FormContact', 
  data(){
    return {
      step: 0,
      user: {
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
    next(){
      return this.step++;
    }, 
    previous(){
      return this.step--;
    }, 
    submit(){
      this.$http.post('https://myportfolio-9a37b.firebaseio.com/contact.json', this.user)
        .then(response => {
          /*eslint-disable */
          console.log(response);
        }, error => {
          console.log(error);
        }) 
    }
  }
} 
</script>

<style lang="scss" scoped>
.main {
  grid-column-start: 2;
  grid-column-end: 3;
  display: grid; 
  grid-template-columns: 33% 33% 33%;
  grid-template-rows: 100%;
  grid-gap: 15px;
  height: 100%;
}
.user {
  grid-column-start: 2;
  grid-column-end: 3;
  padding: 30px;
  border: 1px solid rgb(27, 27, 50);
  border-radius: 5px;
  justify-self: center;
}

::placeholder {
  color: rgb(162, 171, 221);
}
.select {
  border-radius: 5px;
  border: 1px solid rgb(27, 27, 50);
  color: white;
  height: 45px;
  padding: 5px;
  margin: 5px;
}
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
.next {
  background-color:rgb(27, 27, 50);
  padding: 5px;
  border-radius: 5px;
  border: 1px solid rgb(27, 27, 50);
  color: white;
}
.previous {
  background-color: rgb(162, 171, 221);
  padding: 5px;
  border-radius: 5px;
  border: 1px solid rgb(162, 171, 221);
  color: white;
}
</style>
