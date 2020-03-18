<template>
  <div class="main">
    <div class="intro">
      <p> Hello, my name is Thibault, may I ask you a question ? </p>
        <h3> Who has never had a bad user experience on the web? </h3>
          <p> 
            A few months ago, I made a professional transition to web development. 
            I'm a self-taugh, trained with the FreeCodeCamp platform, 
            to evolve towards a job that stimulates me more on a daily basis 
            and allows me to offer a better user experience on the web.
          </p>
    </div>
    <div class="education">
      <h1>Education</h1>
      <ul class="coding">
        <h2>Coding</h2>
          <li>2020 - <strong>Vue.js</strong> (Vue CLI, vueRouter, NUXT.js, Axios, Vuex) - self-taught</li>
          <li>2019 / 2020 - FreeCodeCamp - Front End Libraries Certification (<strong>Sass</strong>, React)</li>
          <li>2019 - FreeCodeCamp - <strong>JavaScript</strong> Algorithms and Data Structures  
          <!-- <a rel="noreferrer" href="">Certification</a></li> -->
          <li>2019 - FreeCodeCamp - Responsive Web Design 
            <a rel="noreferrer" href="https://www.freecodecamp.org/certification/thib-21/responsive-web-design">Certification</a>
            </li>
       </ul> 
       <ul class="projects">
         <h2>Project Management / Innovation / Entrepreneurship</h2>
           <li>2015 / 2017 - Centrale Lyon - emlyon business school - Msc Entrepreneurship & Innovation (design Thinking / Ux design) 
             <a rel="noreferrer" href="https://www.linkedin.com/in/thibault-decousus/?locale=en_US">see more</a>
             </li>
       </ul>
    </div>
    <div class="hobbies">
      <h1>Hobbies</h1>
        <ul class="hobbie">
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
  grid-gap: 5px;

}
.intro{
  background-color: rgb(134, 134, 148);
  border-radius: 5px;
  color: white;
}
p, h3 {
  text-align: center;
  margin: 10px 15px;
  padding: 15px;
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
.education, .projects, .coding, .hobbies, .hobbie {
  padding: 10px;
  margin-top: 10px;
}

</style>
