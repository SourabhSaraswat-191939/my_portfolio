<template>
<div class="home_container">
  <div class="home">
    <!-- <li></li>
    <li></li>
    <li></li>
    <li></li>
    <li></li>
    <li></li>
    <li></li>
    <li></li> -->


    <home_text />
    <rotate_box style="float:right;"/>
  </div>
    <a href="#experience"><down_arrow style="position:absolute;bottom:0;width:100%"/></a>
  
    
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
  background-image: url(../assets/c2.jpg);
  background-size: cover;
  /* background: black; */
  color: #fff;
  position: relative;
  display: flex;
  flex-direction: row;
}

.home_container{
  position: relative;
}
/* 
li{
  border-radius: 100%;
  width: 30px;
  height: 30px;
  margin:20px ;
  list-style: none;
  animation-duration: 4s;
  animation-iteration-count: infinite;
  animation-fill-mode: backward;
  position: absolute;
  background: #fff;
  box-shadow:0px 0px 20px 10px #0ff; 
}

li:nth-child(1){
  animation-name: UpDown;
  animation-delay: 3s;
}

li:nth-child(2){
  animation-name: cross;
  animation-delay: 3s;
}
li:nth-child(3){
  animation-name: cross;

}
li:nth-child(4){
  animation-name: UpDown;
}

li:nth-child(5){
  animation-name: Bounce;
  animation-delay: 3s;
}li:nth-child(6){
  animation-name: Bounce;
}li:nth-child(7){
  animation-name: UpDown;
  animation-delay: 3s;
}li:nth-child(8){
  animation-name: UpDown;
}
@keyframes UpDown {
  0%   {box-shadow:0px 0px 20px 0px #eea849; left:0px; top:0px;}
  25%  {box-shadow:0px 0px 20px 10px #eea849; left:500px; top:0px;}
  50%  {box-shadow:0px 0px 20px 0px #eea849; left:200px; top:800px;}
  75%  {box-shadow:0px 0px 20px 10px #eea849; left:0px; top:900px;}
  100% {box-shadow:0px 0px 20px 0px #eea849; left:0px; top:0px;}
}

@keyframes cross {
  0%   {box-shadow:0px 0px 20px 10p#f46b45; left:0px; top:0px;}
  25%  {box-shadow:0px 0px 20px 0px #f46b45; left:600px; top:100px;}
  50%  {box-shadow:0px 0px 20px 10px #f46b45; left:200px; top:300px;}
  75%  {box-shadow:0px 0px 20px 0px #f46b45; left:400px; top:700px;}
  100% {box-shadow:0px 0px 20px 10px #f46b45; left:0px; top:0px;}
}

@keyframes Bounce {
  0%   {box-shadow:0px 0px 20px 10px #0ff; left:0px; top:0px;}
  25%  {box-shadow:0px 0px 20px 0px #0ff; left:50px; top:300px;}
  40%  {box-shadow:0px 0px 20px 10px #0ff; left:100px; top:40px;}
  50%  {box-shadow:0px 0px 20px 0px #0ff; left:600px; top:10px;}
  60%  {box-shadow:0px 0px 20px 10px #0ff; left:750px; top:300px;}
  75%  {box-shadow:0px 0px 20px 0px #0ff; left:500px; top:800px;}
  100% {box-shadow:0px 0px 20px 10px #0ff; left:0px; top:0px;}
} */



@media only screen and (max-width: 960px) {
  .home{
  background-image: url(../assets/c4.jpg);
  height: auto;
  flex-direction: column;;
}
}


</style>
