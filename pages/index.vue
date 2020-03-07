<template>
  <div class="container">
    <!-- <h1>{{ $t('Welcome') }}</h1> -->
    <div class="welcome">
      <h1>Hi, my name is Thibault. I'm a Front-End Developer. Welcome to my portfolio ! </h1>
    </div>
    <div class="introduction">
     
    
    <img class="avatar" src='https://avataaars.io/?avatarStyle=Circle&topType=ShortHairShortWaved&accessoriesType=Blank&hairColor=Black&facialHairType=BeardLight&facialHairColor=BrownDark&clotheType=GraphicShirt&clotheColor=Blue03&graphicType=Bat&eyeType=Happy&eyebrowType=UpDown&mouthType=Serious&skinColor=Tanned'
/>
    <nuxt />
  </div>
<!-- 
    <nuxt-link
      v-if="$i18n.locale !== 'en'"
      :to="switchLocalePath('en')"
    >
      English
    </nuxt-link>

    <nuxt-link
      v-if="$i18n.locale !== 'fr'"
      :to="switchLocalePath('fr')"
    >
      Español
    </nuxt-link> -->
    
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
h1 {
  text-align: center;
}
.avatar {
  height: 10%;
  width: 10%;
}

</style>
