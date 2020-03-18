<template>
  <div class="main">
    <div class="code">
      <h2>Coding</h2>
      <hr>
      <p><strong>I code with ..</strong></p>
      <ul>
        <li>HTML 5</li>
        <li>CSS 3</li>
        <li>JS - ES6</li>
        <li>Vue.js (VueRouter) Vuex, Nuxt.js</li>
      </ul>
      <p><strong>And I use ..</strong></p>
      <ul>
        <li>VsCode - ES Lint - LightHouse</li>
        <li>GitHub</li>
        <li>WSL - Ubuntu</li>
      </ul>
    </div>
    <div class="projectManagement">
      <h2>Project Management</h2>
      <hr>
       <p><strong>I work with..</strong></p>
      <ul>
        <li>Agile - SCRUM</li>
        <li>Design Thinking</li>
        <li>Lean Startup</li>
      </ul>
       <p><strong>I use..</strong></p>
       <ul>
        <li>Trello</li>
        <li>Jira</li>
        <li>Teams / sharepoint</li>
      </ul>
    </div>
    <div class="uxDesign">
      <h2>Ux Design</h2>
      <hr>
      <p><strong> I design..</strong></p>
      <ul>
        <li>Customer journey</li>
        <li>personae</li>
        <li>Apps (mockup, wireframe)</li>
      </ul>
      <p><strong> I use..</strong></p>
      <ul>
        <li>Xd</li>
        <li>Illustrator</li>
        <li>Launchaco</li>
      </ul>
    </div>
    <nuxt />
  </div>
</template>


<style scoped>
.main {
  display: grid; 
  grid-template-columns: 33% 33% 33%;
  grid-template-rows: 100%; 
  grid-gap : 10px;
  padding: 10px;
  margin: 20px;
  height: 690px;
}
.code {
background-color: rgb(59, 59, 79);
color: rgb(27, 27, 50);
border-radius: 5px;
color: white;
grid-row-start: 1;
grid-row-end: 3;
padding: 15px;
margin: 15px;
height: 100%;
}

.projectManagement {
  background-color: rgb(134, 134, 148);
  color: rgb(27, 27, 50);
  border-radius: 5px;
  color: white;
  grid-row-start: 1;
  grid-row-end: 3;
  padding: 15px;
  margin: 15px;
height: 100%;
}

.uxDesign {
  background-color: rgb(238, 238, 240);
  color: rgb(27, 27, 50);
  border-radius: 5px;
  grid-row-start: 1;
  grid-row-end: 3;
  padding: 10px;
  margin: 15px;
height: 100%;
}

li, h2  {
  list-style-type: none;
  padding: 15px;
}
p {
  padding: 20px;
}
@media only screen and (max-width: 768px) {
  .main {
    
    display: grid; 
    grid-template-columns: 100%;
    grid-template-rows: 100%; 
    grid-gap : 70px;
    padding: 5px;
    height: 100%;
    margin-top: 0px;
   
  }
  .code {
    font-size: 12px;
    grid-column-start: 1;
    grid-column-end: 2;
    grid-row-start: 1;
    grid-row-end: 2;
    height: 110%;
  }
  .projectManagement {
    font-size: 12px;
    grid-column-start: 1;
    grid-column-end: 2;
    grid-row-start: 2;
    grid-row-end: 3;
    height: 110%;
  }
  .uxDesign {
    font-size: 12px;
    grid-column-start: 1;
    grid-column-end: 2;
    grid-row-start: 3;
    grid-row-end: 4;
    height: 110%;
  }
  
}
</style>
