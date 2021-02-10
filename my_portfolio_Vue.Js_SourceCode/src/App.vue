<template>
<v-app>
<div class="main">
  
  <home_front />
  <!-- <div style="height:80vh;position:relative;">Sourabh Saraswat</div> -->
  <about_me id="aboutss" />
</div>
</v-app>
</template>

<script>

import home_front from "./views/home_front"
import about_me from "./components/about_me"

export default {
  name: 'App',

  components:{
    home_front,
    about_me,
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
