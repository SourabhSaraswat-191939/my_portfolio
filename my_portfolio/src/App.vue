<template>
<v-app>
<div class="main">
  
  <home_front />
  <!-- <div style="height:80vh;position:relative;">Sourabh Saraswat</div> -->
  <!-- <about_me /> -->
</div>
</v-app>
</template>

<script>

import home_front from "./views/home_front"
// import about_me from "./components/about_me"

export default {
  name: 'App',

  components:{
    home_front,
    // about_me,
  }
}
</script>


<style scoped>


</style>
