<template>
  <div class="main">
    <div class="code">
      <h2>Code/programmation</h2>
      <hr>
      <p><strong>I code with ..</strong></p>
      <ul>
        <li>HTML 5</li>
        <li>CSS 3</li>
        <li>JS - ES6</li>
        <li>Vue.js (VueRouter, Nuxt.js)</li>
      </ul>
      <p><strong>And I use ..</strong></p>
      <ul>
        <li>VsCode</li>
        <li>GitHub</li>
        <li>Ubuntu</li>
      </ul>
    </div>
    <div class="projectManagement">
      <h2>Project Management</h2>
      <hr>
       <p><strong>I work with some Framework..</strong></p>
      <ul>
        <li>Agile - SCRUM</li>
        <li>Design Thinking</li>
        <li>Lean Startup</li>
      </ul>
       <p><strong>I used somme tools..</strong></p>
       <ul>
        <li>Trello</li>
        <li>Jira</li>
        <li>GitHub</li>
      </ul>
    </div>
    <div class="uxDesign">
      <h2>Ux Design</h2>
      <hr>
      <p><strong> I designed..</strong></p>
      <ul>
        <li>Customer journey</li>
        <li>personae</li>
        <li>Apps (mockup, wireframe)</li>
      </ul>
      <p><strong> I used to..</strong></p>
      <ul>
        <li>xD</li>
        <li>Illustrator</li>
        <li>launchaco</li>
      </ul>
    </div>
    <nuxt />
  </div>
</template>

<script>
export default {
  layout: '',

}
</script>

<style lang="scss" scoped>
.main {
  display: grid; 
  grid-template-columns: 33% 33% 33%;
  grid-template-rows: 10% 80% 20%; 
  grid-gap : 10px;
  padding: 5px;
}
.code {
background-color: rgb(59, 59, 79);
color: rgb(27, 27, 50);
border-radius: 5px;
color: white;
grid-row-start: 1;
grid-row-end: 3;
padding: 10px;

  li {
  list-style-type: none;
  padding: 5px;
  }
}
.projectManagement {
  background-color: rgb(134, 134, 148);
  color: rgb(27, 27, 50);
  border-radius: 5px;
  color: white;
  grid-row-start: 1;
  grid-row-end: 3;
  padding: 10px;

  li {
  list-style-type: none;
  padding: 5px;
  }
}
.uxDesign {
  background-color: rgb(238, 238, 240);
  color: rgb(27, 27, 50);
  border-radius: 5px;
  grid-row-start: 1;
  grid-row-end: 3;
  padding: 10px;

  li {
  list-style-type: none;
  padding: 5px;
  }
  
}
</style>
