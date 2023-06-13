<template>
    <div class="container">
        <!-- <button_popper /> -->
        <img src="../assets/mine.png" height="50%" width="50%"/>
        <br>
        <h1 class="name">SOURABH SARASWAT</h1>
        I am a Full Stack Developer
        
    </div>
</template>


<script>

// import button_popper from "../components/button_popper"

export default {
  name: 'home_text',

  components:{
    // button_popper,
   
  }
}
</script>


<style scoped>

.container{
    display: flex;
    flex-direction: column;
    justify-content: center;
    justify-items: center;
    align-content: center;
    text-align: center;
    
    width: 50%;
    float: left;
    height: 100vh;
    text-shadow: 0 0 10px #f46b45;


}

img{
  margin-left:auto;
  margin-right:auto;
  

}

@media only screen and (max-width: 960px) {
  img{
    width:100% ;
  }
}

</style>