<template>
  <div class="brick-container">
    <div class="static_brick">
      <h2 class="static_title">Statics projects</h2>
        <img class="statics" src="../static/Images/html-css.jpg">
        <!--  ----------> 
      <div class="brick-1">
        <div class="brick_inner">
          <a href="../static/Projects/Totem/index.html" class="inner_image"><img class="totem" src="../static/Projects/Totem_img.png"></a> 
          
          <!-- 
          <div class="brick_details"> je mets la page vers laquelle je veux rediriger nuxt-link ? Créer un composant ?
            <div id="totem_project_img" class="brick-image" style="background-image" url("https://www.dropbox.com/h?preview=Totem_img.png")> 
            -->
          
          </div>          
        </div>  
      
        <div class="brick-2">
        <div class="brick_inner">
          <a href="../static/Projects/Totem/index.html" class="inner_image"><img class="totem" src="../static/Projects/Totem_img.png"></a> 
          <div class="brick_details"> </div>

          <div class="brick_figcaption"> </div>
        </div>
      </div>
      <div class="brick-3">
        <div class="brick_inner">
          <a href="../static/Projects/Totem/index.html" class="inner_image"><img class="totem" src="../static/Projects/Totem_img.png"></a> 
          <div class="brick_details"> </div>

          <div class="brick_figcaption"> </div>
        </div>
      </div>
    </div>
 <!--  ----------> 
     <div class="vue_brick">
       <h2 class="dynamic_title">Vue.js projects</h2>
        <img class="dynamic" src="../static/Images/vue.jpg"><img class="dynamic" src="../static/Images/Sass.png">
        <!--  ----------> 
        <div class="brick">
          <div class="brick_inner">
           <a href="components/Survey/src/App.vue"><video width="320" height="180" controls :src="video">
             <!-- <source src="" type="video/Mp4"> -->
             </video></a>
            <div class="brick_details"> </div>
            <div class="brick_figcaption"> </div>
          </div>
        </div>
    </div>
    <nuxt />      
  </div>
</template>

<script>
// import App from '../components/Survey/src/components/pages/FormPage'
export default {
  // layout: 'default',
  components: {
    // FormPage
  }, 
  data(){
    return {
      video: "static/Projects/SurveyForm.mp4"
    }
  }

}
</script>

<style lang="scss" scoped>
.brick-container {
  display: grid;
  grid-template-columns: 50% 50%;
  grid-template-rows: 15% 25% 25% 25% 15%;
  height: 800px;
  
}
.static_brick {
  grid-column-start: 1;
  grid-column-end: 2;
  grid-row-start: 1;
  grid-row-end: 5;
  margin: 5px;
  padding: 5px;
  background-color: rgb(59, 59, 79);
  border-radius: 5px;
  height: 100%;
  justify-self: center;
}
.statics {
  height: 10%;
  width: 20%;
  border-radius: 5px;
  margin: 10px;
}
.static_title {
  color: white;
  margin: 5px;
}
 a {
  text-decoration: none;
  color: rgb(27, 27, 50);
  list-style-type: none;
  color: white;
  margin: 5px;
}
.totem {
  border: 10px solid white;
  border-radius: 5px;
  margin: 5px;
  height: 100%;
  width: 55%;
}

.vue_brick {
  background-color: rgb(238, 238, 240);
  grid-column-start: 2;
  grid-column-end: 3;
  grid-row-start: 1;
  grid-row-end: 5;
  margin: 5px;
  padding: 5px;
  border: 1px solid rgb(27, 27, 50);
  border-radius: 5px;
  height: 100%;
}
.dynamic {
  height: 10%;
  width: 10%;
  margin: 5px;
}
.dynamic_title {
  margin: 5px;
  color:rgb(27, 27, 50);
}
video {
  border-radius: 5px;
  border: 10px solid white;

}

</style>
