<template>
<div class="main">
  <home_text />
  <rotate_box style="float:right;"/>
  <down_arrow />
</div>
</template>

<script>

import rotate_box from "./components/rotate_box"
import home_text from "./components/home_text"
import down_arrow from "./components/down_arrow"

export default {
  name: 'App',

  components:{
    rotate_box,
    home_text,
    down_arrow,
  }
}
</script>


<style scoped>
.main{
  width: 100%;
  height: 100vh;
  /* background-image: url("./assets/home_back.jpg"); */
  /* background-size: cover; */
  background:black;
  color: #fff;
}
</style>
