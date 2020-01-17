<template>
  <div class="main">
    <h1><img class="statics" src="../static/Images/html-css.jpg">Static projects</h1>
      <ul>
        <li><a href="../static/Projects/index.html">Totem project</a></li>
        <li></li>
        <li></li>
      </ul>
    <h1><img class="dynamic" src="../static/Images/vue.jpg"><img class="dynamic" src="../static/Images/Sass.png">Vue.js projects</h1>
       <ul>
        <li></li>
        <li></li>
        <li></li>
      </ul>
    <nuxt />
  </div>
</template>

<script>
// import App from '../components/Survey/src/components/pages/FormPage'
export default {
  layout: 'default',
  components: {
    // FormPage
  }

}
</script>

<style lang="scss" scoped>

a, li {
  text-decoration: none;
  color: rgb(27, 27, 50);
  list-style-type: none;
}
.statics {
  height: 20%;
  width: 20%;
}
.dynamic {
  height: 10%;
  width: 10%;
}

</style>
