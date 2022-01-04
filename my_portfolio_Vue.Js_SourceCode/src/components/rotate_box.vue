<template>
<div style="position:relative;">
  <center>


<div class="radio-toolbar">
      <input type="radio" checked id="radio-front" name="select-face"/>
        <label for="radio-front">
        Home</label> 

      <input type="radio" id="radio-back" name="select-face"/>
        <label for="radio-back">
        Skills</label>

      <input type="radio" id="radio-top" name="select-face"/>
        <label for="radio-top">
        Projects</label>

      <input type="radio" id="radio-bottom" name="select-face"/>
        <label for="radio-bottom">
        Experience</label>

      <input type="radio" id="radio-left" name="select-face"/>
        <label for="radio-left">
        Social Media</label>

      <input type="radio" id="radio-right" name="select-face"/>
        <label for="radio-right">
        About</label>




  <div class="scene">
  <div v-bind:class="{cube:true}">

    <div v-bind:class="{cube__face:true, cube__face__front:true}">
      <div class="heading">.... Welcome To My Portfolio ....</div>
      <br><br>
      I Create stuff that people want .
      <br><br><br>
      <v-btn
        class="ma-2"
        outlined
        color="indigo"
        href="https://drive.google.com/file/d/1VODVJc-fjm1MaWaeX_hcsbYSk0skHMbs/view?usp=sharing"
        target="_blank"
        
      >
          <v-icon light>mdi-file-document</v-icon>
          My Resume
      </v-btn>
      
    </div>


    <div v-bind:class="{cube__face:true, cube__face__top:true}">
      <div class="heading" style="background:linear-gradient(10deg,#8b75f8,#20bdff,#a5fecb);">Technical Skills</div>
      <br><br>
      <div class="text-center">
        <v-chip v-for="(skill,i) in skills" :key="i" class="ma-2 " color="yellow">
          {{skill}}
        </v-chip>    
      </div>
    </div>
    
    
    
    <div v-bind:class="{cube__face:true, cube__face__right:true}">
      <div class="heading" style="background:linear-gradient(10deg,#FEAC5E,#C779D0,#4BC0C8);">About Me</div>
      <br><br>
      Hi! myself Sourabh Saraswat. I am pursuing my Under-graduation in Computer Science and Engineering from Central University Of Haryana . I am a Full Stack Web Developer .I love to know about technologies and pretty much excited to learn new things of modern technical world .MY greatest strength is my positive attitude , even during the most hardest of times.
      <br>I’m constantly Practicing New Technologies .

    </div>


    <div v-bind:class="{cube__face:true, cube__face__left:true}">
      <div class="heading" style="background: linear-gradient(10deg,#304352,#d7d2cc);">Social Links</div>
      <br>
      <div class="social_links">
        
        <li><v-icon color="#eea849" large>mdi-email-multiple</v-icon> saraswatsourabh5@gmail.com
        </li>
        <li v-for="(social,j) in social_media" :key="j">
        <a :href="social.link" target="_blank">
          <v-icon color="#eea849" large>mdi-{{social.icon}}</v-icon> {{social.name}}
        </a>
        <br>
        </li>
      </div>
    </div>


    <div v-bind:class="{cube__face:true, cube__face__back:true}">
      <div class="heading" style="background: linear-gradient(10deg,#ff4b1f,#64b3f4,#c2e59c);">My Projects</div>
      <br><br>
      
      <v-row id="cube_project" class="mx-auto brown mb-2 rounded-xl"><v-icon>mdi-arrow-right-drop-circle</v-icon>MEDICARES SOLUTIONS</v-row>
      <v-row id="cube_project" class="mx-auto brown mb-2 rounded-xl"><v-icon>mdi-arrow-right-drop-circle</v-icon>FOOD DESK</v-row>
      <v-row id="cube_project" class="mx-auto brown mb-2 rounded-xl"><v-icon>mdi-arrow-right-drop-circle</v-icon>HOSTEL MANAGEMENT</v-row>
      <v-row id="cube_project" class="mx-auto brown mb-2 rounded-xl"><v-icon>mdi-arrow-right-drop-circle</v-icon>MESS MANAGEMENT</v-row>
      <v-row id="cube_project" class="mx-auto brown mb-2 rounded-xl"><v-icon>mdi-arrow-right-drop-circle</v-icon>Medicares Solutions</v-row>

      <v-row id="cube_project" class="mx-auto light-green mt-10 rounded-xl"><v-icon>mdi-arrow-down-drop-circle</v-icon>For Details Scroll Web Page</v-row>


    </div>


    <div v-bind:class="{cube__face:true, cube__face__bottom:true}" style="overflow: scroll;">
      <div class="heading" style="background: linear-gradient(10deg,#43c6ac,#191654);">My Experience</div>
      <br><br>
      
        <v-container>
          <v-row dense>
            <v-col cols="12">
              <v-card
                color="#385F73"
                dark
              >
                <v-card-title class="headline" >
                  <v-icon>mdi-briefcase-outline</v-icon> App Development Intern 
                </v-card-title>
                

                <v-card-subtitle>
                  Internship (Aug. 2021-Oct. 2021)<br>
                  Company : Awechemist Technologies PVT. LTD</v-card-subtitle>
              </v-card>
            </v-col>
          </v-row>
          <v-row dense>
            <v-col cols="12">
              <v-card color="#385F73" dark>
                <v-card-title class="headline" >
                  <v-icon>mdi-briefcase-outline</v-icon> Full Stack Web Developer 
                </v-card-title>
                

                <v-card-subtitle>
                  Internship (Nov. 2020-Jan. 2021)<br>
                  Company : Groocy</v-card-subtitle>
              </v-card>
            </v-col>
          </v-row>
          <v-row dense>
            <v-col cols="12">
              <v-card
                color="#385F73"
                dark
              >
                <v-card-title class="headline" >
                  <v-icon>mdi-briefcase-outline</v-icon> Full Stack Engineer 
                </v-card-title>
                

                <v-card-subtitle>
                  Freelancing (Sep. 2020-Nov. 2020)<br>
                  Company : Medicare Solutions</v-card-subtitle>
              </v-card>
            </v-col>
          </v-row>
          
        </v-container>
        
    </div>

  </div>
  </div>
</div>

  </center>

</div>

</template>

<script>

export default {
  name: 'rotate_box',

  components: {
    
  },

  data: () => ({
    // collapseOnScroll: true,
    skills:['HTML','CSS','JAVASCRIPT','PHP','BOOTSTRAP','PYTHON','DJANGO','MySQL','PostgreSQL','REST API','VUE.js'],
    social_media:[
      {name:'Sourabh Saraswat',link:'https://www.linkedin.com/in/sourabh-saraswat-1681b61a5/',icon:'linkedin'},
      {name:'Sourabh Saraswat 191939',link:'https://github.com/SourabhSaraswat-191939',icon:'github'},
      {name:'@ssaraswat',link:'https://www.instagram.com/ssaraswat/',icon:'instagram'},
      {name:'@SourabhSarasw15',link:'https://twitter.com/SourabhSarasw15',icon:'twitter'},
      {name:'Sourabh Saraswat',link:'https://www.facebook.com/sourabh.saraswat.73/',icon:'facebook'}
    ]
  }),
  methods: {
      
  },
};
</script>

<style scoped>
li{
  list-style: none;
}
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
    background: grey;
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
    background: linear-gradient(120deg,#f46b45,#eea849);
    border-color: #fff;
}

#radio-top:checked ~ .scene .cube{
    background-image: url('/assets/logo.png');
  transform: rotateX(-90deg);
} 
#radio-left:checked ~ .scene .cube{
  transform: rotateY(90deg);
} 
#radio-right:checked ~ .scene .cube{
  transform: rotateY(-90deg);
}
#radio-back:checked ~ .scene .cube{
  transform: rotateY(180deg);
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
  opacity: 0.85;
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

/* .cube__face__front  {background:linear-gradient(0deg,rgb(0, 255, 255),#f38365,#f46b45);color:black; transform: rotateY(  0deg) translateZ(200px); } */
.cube__face__front  {background:linear-gradient(120deg,#f46b45,#eea849);color:black; transform: rotateY(  0deg) translateZ(200px); }
.cube__face__right  {background:linear-gradient(10deg,#FEAC5E,#C779D0,#4BC0C8); transform: rotateY( 90deg) translateZ(200px); }
.cube__face__top   {background:linear-gradient(10deg,#8b75f8,#20bdff,#a5fecb); transform: rotateY(180deg) translateZ(200px); }
.cube__face__left   {background:linear-gradient(10deg,#304352,#d7d2cc);transform: rotateY(-90deg) translateZ(200px); }
.cube__face__back    {background:linear-gradient(10deg,#ff4b1f,#64b3f4,#c2e59c);transform: rotateX( 90deg) translateZ(200px); }
.cube__face__bottom {background:linear-gradient(10deg,#43c6ac,#191654);transform: rotateX(-90deg) translateZ(200px); }

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
.social_links a{
  text-decoration: none;
  text-decoration-color: #fff;
  color: #fff;
}


#cube_project{
  width: 80%;
}


@media only screen and (max-width: 960px) {
  .home_right{
    width: 100%;
    height: auto;
  }
  .scene {
    margin: 0px;
    margin-bottom: 130px;
    width: 320px;
    height: 320px;
    /* border:solid 2px black; */
    perspective: 12100px;
  }

  .cube__face__front  {transform: rotateY(  0deg) translateZ(161px); }
  .cube__face__right  {transform: rotateY( 90deg) translateZ(161px);z-index: 1;}
  .cube__face__back   {transform: rotateY(180deg) translateZ(161px); }
  .cube__face__left   {transform: rotateY(-90deg) translateZ(161px); }
  .cube__face__top    {transform: rotateX( 90deg) translateZ(161px);z-index: 1; }
  .cube__face__bottom {transform: rotateX(-90deg) translateZ(161px); }

  .cube__face{
    overflow: scroll;
  }

  #radio-top:checked ~ .scene .cube{
    background-image: url('/assets/logo.png');
    transform: rotateY(180deg);
  } 
  #radio-back:checked ~ .scene .cube{
    transform: rotateX(-90deg);
  }  
  .v-application .headline{
    font-size: 1.2em !important;
  }
}
</style>
