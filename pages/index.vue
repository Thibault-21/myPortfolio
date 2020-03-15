<template>
  <div class="container">
    <!-- <h1>{{ $t('Welcome') }}</h1> -->
    <div class="introduction">
        <h1>Hi, I'm Thib!</h1> 
        <p>I'm a <strong>Front-End Developer,</strong></p>
        <p>Specialized in <strong>Vue.js</strong>.</p>
        
    </div>
    <div class="picture">    
      <img class="avatar" src='https://avataaars.io/?avatarStyle=Circle&topType=ShortHairShortWaved&accessoriesType=Blank&hairColor=Black&facialHairType=BeardLight&facialHairColor=BrownDark&clotheType=GraphicShirt&clotheColor=Blue03&graphicType=Bat&eyeType=Happy&eyebrowType=UpDown&mouthType=Serious&skinColor=Tanned'
/>
    </div>
    <div class="welcome">
      <h1>Welcome to my portfolio!</h1>
      <p>I hope you will enjoy the experience!</p>
    </div>
     <nuxt />
  </div>
</template>

<script>

import Projects from '../pages/projects'
import Skills from '../pages/skills'
import About from '../pages/about'
import Contact from '../pages/contact'

export default {
  layout: 'default',
  components: {
    Projects,
    Skills,
    About, 
    Contact
  }
}
</script>

<style scoped>
.container {
  display: grid; 
  grid-template-columns: 40% 60%;
  grid-template-rows: 50% 50%;
  grid-gap: 10px;
  height: 610px;
  border: 5px solid rgb(59, 59, 79);
  border-radius: 5px;
  padding: 10px;
  margin: 60px 50px;
}
.picture {
  grid-column-start: 1;
  grid-column-end: 2;
  grid-row-start: 1;
  grid-row-end: 2;

  justify-self: right;
  height: 100%
}
.introduction {
  grid-column-start: 2;
  grid-column-end: 3 ;
  grid-row-start: 1;
  grid-row-end: 2;
  justify-self: left;
  height: 100%;
}
.welcome {
  grid-column-start: 1;
  grid-column-end: 3;
  grid-row-start: 2;
  grid-row-end: 3;

  margin: 0px;
  justify-self: center;
  
}
p, h1 {
  padding: 20px;
  margin: 10px;
  align-self: end;
}
.avatar {
  height: 100%;
  width: 100%;
}
@media only screen and (max-width: 768px) {
  h1 {
    font-size: 16px;
  } 
  .container {
  height: 510px;
  width: 350px;
  border: 5px solid rgb(59, 59, 79);
  border-radius: 5px;
  padding: 10px;
  margin: 60px 20px;
  justify-self: center;
}
.picture {
  grid-column-start: 1;
  grid-column-end: 2;
  grid-row-start: 1;
  grid-row-end: 2;

  justify-self: right;
  height: 100%
}
.introduction {
  grid-column-start: 2;
  grid-column-end: 3 ;
  grid-row-start: 1;
  grid-row-end: 2;
  justify-self: left;
  height: 100%;
}
.welcome {
  grid-column-start: 1;
  grid-column-end: 3;
  grid-row-start: 2;
  grid-row-end: 3;

  margin: 0px;
  justify-self: center;
  
}
.avatar {
  height: 100%;
  width: 100%;
}
}
</style>
