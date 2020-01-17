<template>
  <div class="main">
    <!-- <img src="'./Image/workplace.jpg"> -->
    <header>
      <slot name="header"></slot>
    </header>
    <main>
      <slot></slot>
    </main>
    <footer>
      <slot name="footer"></slot>
    </footer>
  </div>
</template>

<script>
export default {
  name: 'Page',
}
</script>

<style lang="scss" scoped>
.main {
  display: grid;
  grid-template-columns: 30% 80% 30%;
  grid-template-rows: 30% 60% 30%;
}
header, footer { 
  grid-column-start: 2; 
  width: 50%; 
  background-color: rgb(135, 143, 253);
  color: white;
  padding: 5px;
  margin: 2px 0px 5px 5px;
  border-radius: 5px;
}
main { 
  grid-column-start: 2;
  width: 50%; 
  background-color: white;
  color: rgb(0, 0, 0);
  padding: 5px;
  margin: 5px 0px 5px 5px;
  border-radius: 5px;
  border: 1px solid rgb(86, 96, 240);
}

</style>
