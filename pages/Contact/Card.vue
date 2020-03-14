<template>
  <div class="main">
    <div class="card">
      <h1>Thibault Decousus</h1>
      <h3> Front-End Developeur, Specialized in <strong>Vue.js</strong> </h3>
      <hr>
      <p><strong>Contacts: </strong>
        <ul>
          <li><a href="tel:+33699276158">+33699276158</a></li>
          <li>thib.dec.pro@gmail.com</li>
        </ul>
      </p>
    </div>
  </div>
</template>

<script>
export default {

}
</script>

<style scoped>
.main {
  display: grid; 
  grid-template-columns: 33% 33% 33%;
  grid-template-rows: 100%;

  background-color: rgb(27, 27, 50);
  padding: 10px;
}
.card {
  grid-column-start: 2;
  grid-column-end: 3;
  background-color: white; 
  border-radius: 5px;
  margin: 10px;
  padding: 10px;
}
h1, h3 {
  color : rgb(27, 27, 50);
}
li {
  list-style-type: none;
  padding: 10px;
  color : rgb(27, 27, 50);
}
a {
  color : rgb(27, 27, 50);
  font-size: 18px;
}
</style>
