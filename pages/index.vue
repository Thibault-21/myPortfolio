<template>
  <div class="container">
    <!-- <h1>{{ $t('Welcome') }}</h1> -->
    <div class="welcome">
        <p>Hi, I'm Thibault Decousus !</p> 
        <p>I'm a <strong>Front-End Developer,</strong></p>
        <p>Specialized in <strong>Vue.js</strong>.</p>
        <p>Welcome to my portfolio ! </p>
    </div>
    <div class="picture">    
      <img class="avatar" src='https://avataaars.io/?avatarStyle=Circle&topType=ShortHairShortWaved&accessoriesType=Blank&hairColor=Black&facialHairType=BeardLight&facialHairColor=BrownDark&clotheType=GraphicShirt&clotheColor=Blue03&graphicType=Bat&eyeType=Happy&eyebrowType=UpDown&mouthType=Serious&skinColor=Tanned'
/>
    <nuxt />
  </div>

    
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
  grid-template-rows: 100%;
  grid-gap: 10px;
}
.picture {
  grid-column-start: 1;
  grid-column-end: 2;
  grid-row-start: 1;
  justify-self: right;
}
.welcome {
  grid-column-start: 2;
  grid-column-end: 3 ;
  justify-self: left;
}

p {
  padding: 15px;
}
.avatar {
  height: 80%;
  width: 80%;
}
@media only screen and (max-width: 768px) {
  h1 {
    font-size: 16px;
  }
  .avatar {
    height: 80%;
    width: 80%;
  }
}
</style>
