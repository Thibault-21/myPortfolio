<template>
  <div class="main">
    <p>We launch a large survey about the workplace in big companies. This survey can help us to improve your daily work with some new tools</p>
    <button class="btn-n" type="submit" @click.prevent="submitNext">Start</button>
  </div>
</template>

<script>
export default {
  name: 'Form', 
  methods: {
      submitNext() {
        this.$emit('onSubmitNext');
      },
    }
}
</script>

<style lang="scss" scoped>
// @import '../assets/mixins.scss';
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
.main {
  display: flex;
  flex-direction: column;
  align-items: center; 
  // grid-template-columns: 100%;
  // grid-template-rows: 70% 30%;
}
button {
  display: flex;
  justify-content: center; 
}

</style>
