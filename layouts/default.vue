<template>
 <div class="main">
    <Navbar></Navbar>
    <main>
      <nuxt />
    </main>
    <footer>
      <p>&copy 2020 - Thibault Decousus - NUXT.js</p>
    </footer>
  </div>
</template>

<script>
import Navbar from '../components/Navbar/navbar'

export default {
  components: {
    Navbar
  }
}
</script>

<style>
.main {
  font-family: 'Roboto', sans-serif;
}

nav {
  background-color: rgb(27, 27, 50);
  padding: 20px;
  color: white;
}

main {
  /* height: 100%; */
  padding: 10px;
  border-radius: 5px;
  margin: 5px;
  border: 1px solid rgb(27, 27, 50);

  grid-row-start: 2;
  grid-row-end: 3;
}
input {
  height: 20px;
  border-radius: 10px;
  background-color: rgb(59, 59, 79);
  color: white;
  border: 1px solid white;
}

::placeholder {
  padding: 10px;
  color: white;
}

 :focus {
  outline:0 !important;
}

 footer {
  background-color: rgb(238, 238, 240);
  color: rgb(59, 59, 79);
  padding: 25px;
  margin: 5px;
  border-radius: 5px;
}

.spacing{
  color: white;
  margin: 5px;
  padding: 35px;
  border-radius: 5px;
}

.routes, a {
  color: white;
  margin-right: 35px;
  text-decoration: none;
  font-size: 20px;
}
@media only screen and (max-width: 768px) {
 
  nav {
    display: grid; 
    grid-template-columns: 20% 20% 20% 20%; 
    grid-template-rows: 50% 50%; 
    grid-gap: 10px;
    padding: 10px;

    grid-row-start: 1;
    grid-row-end: 2;
  }
  .spacing {
    padding: 20px;
  }
  a {
    margin: 10px;
    padding: 10px;
  }
  .routes {
    margin-right: 35px;
  }

  main {
    display: grid;
    grid-template-columns: 100%;
    grid-template-rows: 25% 25% 25% 25%;
    /* height: 730px; */
  }
}
</style>
