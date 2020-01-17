<template>
  <form method="POST"> 
    <p>Which tools do you use for store your documents ? </p>
      <label for="mailBox">mailBox</label>
      <input type="radio" name="storage" value="mailBox" v-model="storage"/>

      <label for="google_drive">google drive</label>
      <input type="radio" name="storage" value="google_drive" v-model="storage"/>

      <label for="iCloud">iCloud</label>
      <input type="radio" name="storage" value="iCloud" v-model="storage"/>

      <label for="DropBox">DropBox</label>
      <input type="radio" name="storage" value="DropBox" v-model="storage"/>
    
    <button class="btn-s" type="submit" value="Next" @click.prevent="submit"> Submit </button>
    <button class="btn-p" type="submit" value="previous" @click.prevent="submitPrev"> Back </button>
    
  </form>
</template>

<script>
  export default {
    name: 'Form3',
    data(){
      return {
        storage: []
      }
    },
    methods: {
      submitPrev(){
        this.$emit('onSubmitPrev');
      }, 
      submit(){
        this.$emit('onSubmit');
      }
    }
   }
</script>

<style lang="scss" scoped>
// @import '../style/mixins.scss';

form {
    padding: 15px;


  p {
      margin : 20px;
      padding: 10px;
    }

  input {
    padding: 20px;
    margin: 10px;
    color: rgb(86, 96, 240);
  }
@mixin button-submit($bg-color, $color, $height, $width, $margin, $padding, $b-radius, $cursor, $border){
  background-color: $bg-color;
  color: $color;
  height : $height; 
  width: $width; 
  margin: $margin; 
  padding: $padding; 
  border-radius: $b-radius; 
  cursor: $cursor;
  border: $border;
}
  .btn-s {
    @include button-submit(rgb(16, 204, 100), white, 35px, 80px, 5px, 5px, 5px, pointer, 1px solid rgb(16, 204, 100));
  }
  .btn-s:hover {
    @include button-submit(rgb(0, 255, 115), white, 35px, 80px, 5px, 5px, 5px, pointer, 1px solid rgb(0, 255, 115));
  }
}
@mixin button-prev($bg-color, $color, $height, $width, $margin, $padding, $b-radius, $cursor, $border){
  background-color: $bg-color;
  color: $color;
  height : $height; 
  width: $width; 
  margin: $margin; 
  padding: $padding; 
  border-radius: $b-radius; 
  cursor: $cursor;
  border: $border;
}
.btn-p {
  @include button-prev(rgb(140, 73, 146), white, 35px, 80px, 5px, 5px, 5px, pointer, 1px solid rgb(140, 73, 146));
}
.btn-p:hover {
  @include button-prev(rgb(69, 40, 71), white, 35px, 80px, 5px, 5px, 5px, pointer, 1px solid rgb(69, 40, 71));
}

</style>
