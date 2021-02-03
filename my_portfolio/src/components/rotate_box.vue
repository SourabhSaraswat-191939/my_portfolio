<template>
<div>
  <center>


<div class="radio-toolbar">
      <input type="radio" checked id="radio-front" name="select-face"/>
  <label for="radio-front">
        Home</label> 

      <input type="radio" id="radio-back" name="select-face"/>
        <label for="radio-back">
        Details</label>

      <input type="radio" id="radio-left" name="select-face"/>
        <label for="radio-left">
        Social Media</label>

      <input type="radio" id="radio-right" name="select-face"/>
        <label for="radio-right">
        About</label>

      <input type="radio" id="radio-top" name="select-face"/>
        <label for="radio-top">
        Projects</label>

      <input type="radio" id="radio-bottom" name="select-face"/>
        <label for="radio-bottom">
        Experience</label>




  <div class="scene">
  <div v-bind:class="{cube:true,show_front:class_list==='back'}">

    <div v-bind:class="{cube__face:true, cube__face__front:true}">
      <div class="heading">.... Welcome To My Portfolio ....</div>
      <br><br>
      Make stuff that people wants
      
    </div>


    <div v-bind:class="{cube__face:true, cube__face__back:true, show_right:class_list==='back'}"></div>
    <div v-bind:class="{cube__face:true, cube__face__right:true, show_back:class_list==='right'}">right</div>


    <div v-bind:class="{cube__face:true, cube__face__social_links:true, show_left:class_list==='left'}">
      <div class="heading" style="background: linear-gradient(10deg,#304352,#d7d2cc);">Social Links</div>
      <br><br>
      <div class="social_links">
        <v-icon large>mdi-email-multiple</v-icon> saraswatsourabh5@gmail.com
        <br>
        <a href="https://www.linkedin.com/in/sourabh-saraswat-1681b61a5/" target="_blank">
          <v-icon  large>mdi-linkedin</v-icon> Sourabh Saraswat
        </a>
        <br>
        <a href="https://www.instagram.com/ssaraswat/" target="_blank">
          <v-icon  large>mdi-instagram</v-icon> @ssaraswat
        </a>
        <br>
        <a href="https://twitter.com/SourabhSarasw15" target="_blank">
          <v-icon  large>mdi-twitter</v-icon> @SourabhSarasw15
        </a>
        <br>
        <a href="https://www.facebook.com/sourabh.saraswat.73/" target="_blank">
          <v-icon color="green darken-2"  large>mdi-facebook</v-icon> Sourabh Saraswat
        </a>
      </div>
    </div>
    <div v-bind:class="{cube__face:true, cube__face__top:true, show_top:class_list==='top'}">top</div>
    <div v-bind:class="{cube__face:true, cube__face__bottom:true, show_bottom:class_list==='bottom'}">bottom</div>

  </div>
  </div>
</div>

  </center>

</div>

</template>

<script>
// import Login from './components/Login';

export default {
  name: 'App',

  components: {
    // Login,
  },

  data: () => ({
    // collapseOnScroll: true,
    
  }),
  methods: {
      
  },
};
</script>

<style scoped>
.radio-toolbar {
  margin: 10px;
  position: relative;
}

.radio-toolbar input[type="radio"] {
  /* opacity: 0; */
  position:absolute;
  opacity: 0;
  border: solid red 2px;
  width: 10px;
}

.radio-toolbar label {
    display: inline-block;
    background: linear-gradient(120deg,#f46b45,#eea849);;
    padding: 10px 20px;
    margin: 5px;
    font-family: sans-serif, Arial;
    font-size: 16px;
    border: 2px solid #444;
    border-radius: 4px;
    cursor: pointer;
}

.radio-toolbar label:hover {
  background:#eea849;
}

.radio-toolbar input[type="radio"]:focus + label {
    border: 2px dashed #444;
}

.radio-toolbar input[type="radio"]:checked + label {
    background: linear-gradient(120deg,#f46b45,#eea849);;
    border-color: #fff;
}

#radio-back:checked ~ .scene .cube{
    background-image: url('/assets/logo.png');
  transform: rotateY(180deg);
} 
#radio-left:checked ~ .scene .cube{
  transform: rotateY(90deg);
} 
#radio-right:checked ~ .scene .cube{
  transform: rotateY(-90deg);
}
#radio-top:checked ~ .scene .cube{
  transform: rotateX(-90deg);
}  
#radio-bottom:checked ~ .scene .cube{
  transform: rotateX(90deg);
}


.change{
    
    background:yellow;
}

.scene {
  margin: 130px;
  width: 400px;
  height: 400px;
  /* border:solid 2px black; */
  perspective: 600px;
}

.cube {
  position: relative;
  width: inherit;
  height: inherit;
  transition: all 0.85s cubic-bezier(0.175,0.885,0.320,1.275);
  transform-style: preserve-3d;
  transform: rotateY(180deg);
}

.cube__face {
  width: inherit;
  height: inherit;
  position: absolute;
  background: red;
  opacity: 1;
  text-align: center;
  
}

.cube { 
  margin-top:10vh ;
  transform: translateZ(00px); 
  }

.cube__face__front  {background:#fff;color:black; transform: rotateY(  0deg) translateZ(200px); }
.cube__face__right  { transform: rotateY( 90deg) translateZ(200px); }
.cube__face__back   {background:blue; transform: rotateY(180deg) translateZ(200px); }
.cube__face__social_links   {background:linear-gradient(10deg,#304352,#d7d2cc);transform: rotateY(-90deg) translateZ(200px); }
.cube__face__top    { transform: rotateX( 90deg) translateZ(200px); }
.cube__face__bottom { transform: rotateX(-90deg) translateZ(200px); }

/* 
.show_front  { transform: translateZ(-100px) rotateY(   0deg); }
.show_right  { transform: translateZ(-100px) rotateY( -90deg); }
.show_back   { transform: translateZ(-100px) rotateY(-180deg); }
.show_left   { transform: translateZ(-100px) rotateY(  90deg); }
.show_top    { transform: translateZ(-100px) rotateX( -90deg); }
.show_bottom:hover { transform: translateZ(-100px) rotateX(  90deg); } */



.heading{
  margin-top:10%;
  font-size:1.7em;
  font-weight: 700;
  
}

.social_links{
  margin-left: 10%;
  text-align: left;
}
a{
  text-decoration: none;
  color: #fff;
}
</style>
