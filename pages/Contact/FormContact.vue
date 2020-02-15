<template>
  <form action="" method="PUT" class="main">
   <div class="user">
     <label v-if="step === 0" class="firstPage">
      <select v-model="user.gender">
       <option disabled value="">Please Select Your Gender</option>
       <option value="Mrs">Mrs</option>
       <option value="Mr">Mr</option>
       <option value="Other">Other</option>
      </select>
      <button @click.prevent.enter="next" class="next">Next</button>
     </label>
     <!--  -->
     <label v-else-if="step === 1" class="page">
      <button @click.prevent="previous" class="previous">Back</button>
      <input type="text" v-model="user.firstName" placeholder="Your firstName">
      <button @click.prevent.enter="next" class="next">Next</button>
     </label>
     <!--  -->
     <label v-else-if="step === 2" class="page">
      <button @click.prevent="previous" class="previous">Back</button>
      <input type="text" v-model="user.lastName" placeholder="Your lastName">
    <button @click.prevent.enter="next" class="next">Next</button>
     </label>
     <!--  -->
     <label v-else-if="step === 3" class="page">
      <button @click.prevent="previous" class="previous">Back</button>
      <input type="text" v-model="user.company" placeholder="Your company">
      <button @click.prevent.enter="next" class="next">Next</button>
     </label>
     <!--  -->
     <label v-else-if="step === 4" class="page">
      <button @click.prevent="previous" class="previous">Back</button>
       <input type="text" v-model="user.job" placeholder="Your job">
      <button @click.prevent.enter="next" class="next">Next</button>
     </label>
    <!--  -->
     <label v-else-if="step === 5" class="page">
      <button @click.prevent="previous" class="previous">Back</button>
      <input type="tel" name="phone" pattern="[0-9]{2}-[0-9]{2}-[0-9]{2}-[0-9]{2}-[0-9]{2}" required v-model="user.phone" placeholder="Your phone">
      <button @click.prevent.enter="next" class="next">Next</button>
     </label>
    <!--  -->
     <label v-else-if="step === 6" class="page">
      <button @click.prevent="previous" class="previous">Back</button>
      <input type="text" v-model="user.email" placeholder="Your email">
     <button @click.prevent.enter="next" class="next">Next</button>
     </label>
    <!--  -->
    <label v-else-if="step === 7" class="page">
      <button @click.prevent="previous" class="previous">Back</button>
      <textarea v-model="user.request" placeholder="Your request here.."></textarea>
      <button class="btn-s" type="submit" @click="submit">Submit</button>
     </label>
    <p v-else-if="step === 8"> {{thank}} {{user.gender}} {{user.lastName}}</p>
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
        request: ''
      }, 
      thank: 'Thank you very much'
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
        }); 
        this.step++;
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
  grid-template-rows: 70% 30%;
  grid-gap: 20px;
  height: 100%;
  padding: 30px;
  margin: 20px;
}
.user {
  grid-column-start: 2;
  grid-column-end: 3;
  padding: 30px;
  border: 1px solid rgb(27, 27, 50);
  border-radius: 5px;
  justify-self: center;
  background-color: rgb(27, 27, 50);
  height: 100%;
}
.page {
  grid-column-start: 2;
  grid-column-end: 4;
  grid-row-start: 1;
  grid-row-end: 2;

  display: grid; 
  grid-template-columns: 20% 60 20%;
  grid-template-rows: 100%;
  grid-gap: 10px;

}
input {
  grid-column-start: 2;
  grid-column-end: 3;
  grid-row-start: 1;
  grid-row-end: 2;
  background-color: white;
  color:rgb(27, 27, 50);
  padding: 15px;
  border-radius: 5px;
}
input::placeholder {
  color: rgb(27, 27, 50);
}
select {
  grid-column-start: 1;
  grid-column-end: 4;
  grid-row-start: 1;
  grid-row-end: 2;

  border-radius: 5px;
  border: 1px solid rgb(27, 27, 50);
  color: rgb(27, 27, 50);
  height: 45px;
  padding: 10px;
  margin: 5px;
}
.btn-s {
  grid-column-start: 4;
  grid-row-start: 5;
  grid-row-start: 1;
  grid-row-end: 2;

  border-radius: 5px;
  background-color: white;
  color: rgb(27, 27, 50);
  border: 1px solid rgb(27, 27, 50);
  height: 45px;
  padding: 10px;
  margin: 5px;
}
.next {
  grid-column-start: 4;
  grid-column-end: 5;
  grid-row-start: 1;
  grid-row-end: 2;

  background-color:rgb(27, 27, 50);
  padding: 10px;
  margin: 10px;
  border-radius: 5px;
  border: 1px solid white;
  color: white;
}
.previous {
  grid-column-start: 1;
  grid-column-end: 2;
  grid-row-start: 1;
  grid-row-end: 2;

  background-color: rgb(162, 171, 221);
  padding: 10px;
  margin: 10px;
  border-radius: 5px;
  border: 1px solid rgb(162, 171, 221);
  color: white;
}
</style>
