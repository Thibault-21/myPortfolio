<template>
  <form method="POST">
    <p>Which tools do use use for communicate ?</p>
    <label for="skype"> Skype</label> 
    <!-- name : doit être le même pour tous les input pour que -->
    <!-- je puisse les regrouper dans un seul et même tableau --> 
    <input type="checkbox" name="communication" value="skype" v-model="communication"/><br>
    <label for="skype"> Webex</label>
    <input type="checkbox" name="communication" value="Webex" v-model="communication"/><br>
    <label for="skype"> mailBox</label>
    <input type="checkbox" name="communication" value="mailBox" v-model="communication"/><br>

    <button class="btn-p" type="submit" value="previous" @click.prevent="submitPrev"> Back </button>
    <button class="btn-n" type="submit" value="Next" @click.prevent="submitNext"> Next </button>
  </form>
</template>

<script>
export default {
  name: 'Form2',
  data(){
    return {
      communication: []
    }
  },
  methods: {
    submitNext(){
      this.$emit('onSubmitNext');
    }, 
    submitPrev(){
      this.$emit('onSubmitPrev');
    }
  }
}
</script>

<style lang="scss" scoped>
// @import '../style/mixins.scss';
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
@mixin button-next($bg-color, $color, $height, $width, $margin, $padding, $b-radius, $cursor, $border, $display){
    
    background-color: $bg-color;
    color: $color;
    height : $height; 
    width: $width; 
    margin: $margin; 
    padding: $padding; 
    border-radius: $b-radius; 
    cursor: $cursor;
    border: $border;
    grid-column-start: $display;
  }
  .btn-n {
    @include button-next(rgb(86, 96, 240), white, 35px, 80px, 5px, 5px, 5px, pointer, 1px solid rgb(86, 96, 240), 3);
  }
  .btn-n:hover {
    @include button-next(rgb(154, 161, 255), white, 35px, 80px, 5px, 5px, 5px, pointer, 1px solid rgb(154, 161, 255), 3);
  }

  form {
    border-radius: 5px;
    padding: 20px;
  }
  input {
    padding: 15px;
    margin: 10px;
    color: rgb(86, 96, 240);
  }

</style>
