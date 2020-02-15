<template>
  <div class="main">
    <p>I would like to ask you a question: 
      - Who has never had a bad user experience on the web? 
      Hello, my name is Thibault, and I'm a front-end developer. I training on my own and with FreeCodeCamp, to evolve towards better, more challenging work at the heart of technology to design and code better user experiences. </p>
    <div class="education">
      <h1>Education</h1>
      <ul class="coding">
        <h2>Coding</h2>
          <li>2020 - <strong>Vue.js</strong> (Vue CLI, vueRouter, NUXT.js, Axios, Vuex) - on my own</li>
          <li>2019 / 2020 - FreeCodeCamp - Front End Libraries Certification (<strong>Sass</strong>, React)</li>
          <li>2019 - FreeCodeCamp - <strong>JavaScript</strong> Algorithms and Data Structures  <a href="">Certification</a></li>
          <li>2019 - FreeCodeCamp - Responsive Web Design <a href="https://www.freecodecamp.org/certification/thib-21/responsive-web-design">Certification</a></li>
        <h2>Project Management / Innovation / Entrepreneurship</h2>
          <li>2015 / 2017 - Centrale Lyon - emlyon business school - Msc Entrepreneurship & Innovation (design Thinking / Ux design) <a href="https://www.linkedin.com/in/thibault-decousus/?locale=en_US">see more</a></li>
      </ul>
    </div>
    <div class="hobbies">
      <h1>Hobbies</h1>
        <ul>
          <li>Theatre within a band</li>
          <li>Chess</li>
          <li>Sports (running & swimming)</li>
        </ul>
    </div>
  </div>
</template>

<script>
export default {
  layout: '',

}
</script>

<style scoped>
.main {
  font-family:Arial, Helvetica, sans-serif;
  color:rgb(27, 27, 50);
  display: grid; 
  grid-template-columns: 100%;
}

.btn {
  border-radius: 5px;
  border: 1px solid rgb(134, 134, 148);
  background-color: rgb(134, 134, 148);
  color: white;
  height: 25px;
  padding: 5px;

}
a {
  color: rgb(134, 134, 148);
  font-size: 16px;
}
li {
  padding: 10px;
  margin: 5px;
}
</style>
