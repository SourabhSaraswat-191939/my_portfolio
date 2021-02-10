<template>
<div class="home_container">
  <div class="home">
    <home_text />
    <rotate_box style="float:right;"/>
  </div>
    <a href="#aboutss"><down_arrow style="position:absolute;bottom:0;width:100%"/></a>
  
    
</div>
</template>

<script>

import rotate_box from "../components/rotate_box"
import home_text from "../components/home_text"
import down_arrow from "../components/down_arrow"
// import about_me from "../components/about_me"

export default {
  name: 'home_front',

  components:{
    rotate_box,
    home_text,
    down_arrow,
    // about_me,
  },
  
}

</script>


<style scoped>
.home{
  width: 100%;
  height: 100vh;
  background:black;
  color: #fff;
  position: relative;
  display: flex;
  flex-direction: row;
}

.home_container{
  position: relative;
}

@media only screen and (max-width: 960px) {
  .home{
  
  height: auto;
  flex-direction: column;;
}
}


</style>
