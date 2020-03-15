<template>
  <div class="main">
    <div class="card">
      <h1>Thibault Decousus</h1>
      <h3> Front-End Developeur, </h3> 
      <p>Specialized in <strong>Vue.js</strong> </p>
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
  grid-template-rows: 50% 50%;

  background-color: rgb(27, 27, 50);
  border-radius: 5px;
  padding: 80px;
  margin: 25px;
  
}
.card {
  grid-column-start: 2;
  grid-column-end: 3;
  grid-row-start: 1;
  grid-row-end: 3;
  background-color: white; 
  border-radius: 5px;
  margin: 20px;
  padding: 50px;
  height: 100%;
}
h1, h3, p {
  color : rgb(27, 27, 50);
  margin-top: 20px;
  padding: 15px;
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
@media only screen and (max-width: 768px) {
  .main {
    display: grid;
    grid-gap: 5px;
    padding: 25px;
    margin: 5px;
    height: 600px;
   
  }
  .card {
    grid-column-end: 4;
    grid-column-start: 1;
    grid-row-end: 1;
    grid-row-start: 3;
    margin: 10px;
    padding: 5px;
     
  }
}
</style>
