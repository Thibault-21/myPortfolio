<template>
 <div class="main">
    <Navbar></Navbar>
    <main>
      <nuxt />
    </main>
    <footer>
    </footer>
  </div>
</template>

<script>
import Navbar from '../components/navbar'

export default {
  components: {
    Navbar
  }
}
</script>

<style lang="scss">


nav {
  background-color: rgb(27, 27, 50);
  padding: 20px;
  color: white;
}
main {
  height: 100%;
  padding: 20px;
  border-radius: 5px;
  margin: 5px;
  border: 1px solid rgb(27, 27, 50);
}
 footer {
  background-color: rgb(162, 171, 221);
  color: white;
  padding: 25px;
  margin: 5px;
  border-radius: 5px;
}

.spacing{
  color: white;
  margin: 5px;
  padding: 25px;
  border-radius: 5px;
}
.routes, a {
  color: white;
  margin-right: 15px;
  text-decoration: none;
}

</style>
