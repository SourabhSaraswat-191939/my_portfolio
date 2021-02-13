<template>
<v-app>
  <div class="main">
    
    <home_front />
    <!-- <div style="height:80vh;position:relative;">Sourabh Saraswat</div> -->
    <!-- <about_me id="aboutss" /> -->
    <experience />
    <projects />
    <footerr />
  </div>
</v-app>
</template>

<script>

import home_front from "./views/home_front"
// import about_me from "./components/about_me"

import experience from './components/experience.vue'
import projects from './components/projects.vue'
import footerr from './components/footer.vue'


export default {
  name: 'App',

  components:{
    home_front,
    // about_me,
    experience,
    projects,
    footerr
  }
}
</script>

<style>
html{
  scroll-behavior: smooth;
}
</style>


<style scoped>


</style>
