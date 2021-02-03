<template>
    <div class="container">
        <!-- <button_popper /> -->
        <h1 class="name">SOURABH SARASWAT</h1>
        <sub_text>I am a Full Stack Web Developer</sub_text>
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
    align-content: center;
    text-align: center;
    border: solid red 2px;
    width: 50%;
    float: left;
    height: 100vh;


}

.name{

}
</style>