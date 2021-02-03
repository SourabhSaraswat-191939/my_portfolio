<template>
<div>
  <center>


<div class="radio-toolbar">
      <input type="radio" :checked="front" id="radio-front" name="select-face"/>
  <label for="radio-front" @click="front!=front">
        On</label> 

      <input type="radio" :checked="back" id="radio-back" name="select-face"/>
        <label for="radio-back" @click="back!=back">
        On</label>

      <input type="radio" v-model="left" id="radio-left" name="select-face"/>
        <label for="radio-left" @click="left!=left">
        On</label>

      <input type="radio" v-model="right" id="radio-right" name="select-face"/>
        <label for="radio-right" @click="right!=right">
        On</label>

      <input type="radio" v-model="top" id="radio-top" name="select-face"/>
        <label for="radio-top" @click="top!=top">
        On</label>

      <input type="radio" v-model="bottom" id="radio-bottom" name="select-face"/>
        <label for="radio-bottom" @click="bottom!=bottom">
        On</label>
  <div class="scene">
  <div v-bind:class="{cube:true,show_front:class_list==='back'}">
    <div v-bind:class="{cube__face:true, cube__face__front:true}">front</div>
    <div v-bind:class="{cube__face:true, cube__face__back:true, show_right:class_list==='back'}">back</div>
    <div v-bind:class="{cube__face:true, cube__face__right:true, show_back:class_list==='right'}">right</div>
    <div v-bind:class="{cube__face:true, cube__face__left:true, show_left:class_list==='left'}">left</div>
    <div v-bind:class="{cube__face:true, cube__face__top:true, show_top:class_list==='top'}">top</div>
    <div v-bind:class="{cube__face:true, cube__face__bottom:true, show_bottom:class_list==='bottom'}">bottom</div>

  </div>
  </div>
</div>

  </center>
  <div v-bind:class="{change:true, mystyle:class_list}"></div>
  <button @click="rotate">left</button>
    
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
    class_list:false,


    front:true,
    back:false,
    left:false,
    right:false,
    top:false,
    bottom:false,
  }),
  methods: {
      rotate(){
            this.class_list = 'back'
      }
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
    background-color: #ddd;
    padding: 10px 20px;
    font-family: sans-serif, Arial;
    font-size: 16px;
    border: 2px solid #444;
    border-radius: 4px;
}

.radio-toolbar label:hover {
  background-color: #dfd;
}

.radio-toolbar input[type="radio"]:focus + label {
    border: 2px dashed #444;
}

.radio-toolbar input[type="radio"]:checked + label {
    background-color: #bfb;
    border-color: #4c4;
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
  margin: 100px;
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
  opacity: 0.8;
}

.cube { transform: translateZ(-100px); }

.cube__face__front  {background:yellow; transform: rotateY(  0deg) translateZ(200px); }
.cube__face__right  { transform: rotateY( 90deg) translateZ(200px); }
.cube__face__back   {background:blue; transform: rotateY(180deg) translateZ(200px); }
.cube__face__left   { transform: rotateY(-90deg) translateZ(200px); }
.cube__face__top    { transform: rotateX( 90deg) translateZ(200px); }
.cube__face__bottom { transform: rotateX(-90deg) translateZ(200px); }

/* 
.show_front  { transform: translateZ(-100px) rotateY(   0deg); }
.show_right  { transform: translateZ(-100px) rotateY( -90deg); }
.show_back   { transform: translateZ(-100px) rotateY(-180deg); }
.show_left   { transform: translateZ(-100px) rotateY(  90deg); }
.show_top    { transform: translateZ(-100px) rotateX( -90deg); }
.show_bottom:hover { transform: translateZ(-100px) rotateX(  90deg); } */


</style>
