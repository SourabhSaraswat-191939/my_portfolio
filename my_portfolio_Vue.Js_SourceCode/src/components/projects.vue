<template>
<div id="projects">
    <v-card class="events-heading" > Projects
    </v-card>

    


    <v-card class="d-flex flex-wrap">
        <v-hover
        v-for="(project,i) in projects"
        :key=i
        v-slot="{ hover }">
            <v-card
            
            class="mx-auto ma-8"
            color="grey lighten-4"
            width="400"
            max-width="600"
            >
            <v-img
                :aspect-ratio="16/9"
                :src="project.image[0]"
            >
                <v-expand-transition>
                <div
                    v-if="hover"
                    class="d-flex transition-fast-in-fast-out orange darken-2 v-card--reveal display-3 white--text"
                    style="height: 100%"
                >
                    {{project.name}}
                    
                </div>
                </v-expand-transition>
            </v-img>
                <v-card-text
        class="pt-6"
        style="position: relative;"
      >
        <h3 class="display-1 font-weight-light orange--text mb-2">
          {{project.name}}
        </h3>
        


            <template>
            <div class="text-center">
                <v-dialog
                v-model="project.dialog"
                width="900"
                height="10"
                >
                <template v-slot:activator="{ on, attrs }">
                    <v-btn
                    class="ma-2"    
                    color="pink"
                    outlined
                    v-bind="attrs"
                    v-on="on"
                    @click="project.dialog=true"
                    >
                    Learn More
                    </v-btn>
                </template>

                <v-card>
                    <v-card-title class="headline grey lighten-2">
                    {{project.name}}
                    </v-card-title>
                    



                    <!-- project image slider start -->
                    <div>
                        
                        <v-carousel v-model="project.model">
                        <v-carousel-item
                            v-for="(image, j) in project.image"
                            :key="j"
                            :src="image"
                        >
                            
                        </v-carousel-item>
                        </v-carousel>
                    </div>
                    <!-- project image slider end -->






                    <v-card-text>
                    <b>{{project.projectType}}</b>
                    </v-card-text>
                    <v-card-text>
                         <h4>About Project</h4>
                    {{project.about}}
                    </v-card-text>

                    <v-divider></v-divider>
                    <v-card-text>
                        <h4>Project Link</h4>
                    <a :href="project.link" target="_blank">{{project.link}}</a>
                    </v-card-text>
                    <v-divider></v-divider>
                    <v-card-text>
                        <h4>Technologies Used</h4>
                    {{project.techUsed}}
                    </v-card-text>
                    <v-divider></v-divider>
                    <v-card-text>
                        <h4>Time Taken</h4>
                    {{project.time}}
                    </v-card-text>
                    <v-card-actions>
                    <v-spacer></v-spacer>
                    <v-btn
                        color="primary"
                        
                        @click="project.dialog = false"
                    >
                    Close
                    </v-btn>
                    </v-card-actions>
                </v-card>
                </v-dialog>
        </div>
        </template>





            </v-card-text>
            </v-card>
        </v-hover>
    </v-card>

    

</div>
</template>

<script>
export default {
    data(){
        return{
            
            
            projects:[
                {
                    name:'Medicares Solutions',
                    about:'It\'s a platform of a private Company by which they sell their medical products online .Their are multiple features including order status , online payment ,search, email verification, order tracking etc., which will be so helpfull for users . Below this i am not sharing server code ,only fronthand code is shared because of Project Security .',
                    link:'https://github.com/SourabhSaraswat/Medicare_Solutions_Fronthand.git',
                    time:'Sep 2020 - Oct 2020',
                    projectType:'FreeLancing',
                    image:[require('@/assets/project_medicare1.png'),require('@/assets/project_medicare2.png'),require('@/assets/project_medicare3.png'),require('@/assets/project_medicare4.png'),require('@/assets/project_medicare5.png')],
                    dialog : false,
                    model: 0,
                    techUsed:'Vue.Js, Django, Django Rest API\'s, Vuetify, PostgreSQL .'
                },
                {
                    name:'Food Desk',
                    about:'This Is a food ordering app , in which user can order food and make payment online from his favourite stores .Multiple Seller can sell their foods , and their is one admin who manages all the seller, client and have whole control over this platform.',
                    link:'https://github.com/SourabhSaraswat/Food-Desk.git',
                    time:'Jun 2020 - Aug 2020',
                    projectType:'Private Project',
                    image:[require('@/assets/project_FoodDesk1.png'),require('@/assets/project_FoodDesk2.png')],
                    dialog : false,
                    model: 0,
                    techUsed:'Vue.Js, Django, Django Rest API\'s, Vuetify, Bootstrap, PostgreSQL .'
                },
                {
                    name:'Hostel Management',
                    about:'This project is to make the student hostel payments digitally in my university. Without any paperworks.',
                    link:'https://github.com/SourabhSaraswat/Hostel-Management.git',
                    time:'Jan 2020 - Feb 2020',
                    projectType:'Private Project',
                    image:[require('@/assets/project_Hostel1.png'),require('@/assets/project_Hostel2.png'),require('@/assets/project_Hostel3.png'),require('@/assets/project_Hostel4.png')],
                    dialog : false,
                    model: 0,
                    techUsed:'HTML, CSS, JavaScript, PHP, MySQL.'
                },
                
                {
                    name:'Mess Management',
                    about:'This project is for the maintenance of record of student going and coming from home .So that food wastage can be prevented . and also saves the money of student who payed for monthly as per university rules.',
                    link:'https://github.com/SourabhSaraswat/Mess_Management.git',
                    time:'Jan 2020 - Feb 2020',
                    projectType:'Private Project',
                    image:[require('@/assets/project_Mess1.png'),require('@/assets/project_Mess2.png'),require('@/assets/project_Mess3.png')],
                    dialog : false,
                    model: 0,
                    techUsed:'HTML, CSS, JavaScript, PHP, MySQL.'
                },
                {
                    name:'Portfolio',
                    about:'This is my Portfolio showing all my skills and some of my projects. You guessed it right! It\'s the one you are looking at right now .',
                    link:'https://github.com/SourabhSaraswat/my_portfolio',
                    time:'5 Days',
                    projectType:'Private Project',
                    image:[require('@/assets/project_portfolio1.png'),require('@/assets/project_portfolio2.png')],
                    dialog : false,
                    model: 0,
                    techUsed:'Vue.Js, Vuetify .'
                },
                {
                    name:'Video Conferecing WebApp UI',
                    about:'This is a UI design of Video Conferencing app for Student-Teacher online meetings .',
                    link:'https://github.com/SourabhSaraswat/Video_Meeting_App',
                    time:'3 Days',
                    projectType:'Private Project',
                    image:[require('@/assets/project_VideoConf1.png'),require('@/assets/project_VideoConf2.png'),require('@/assets/project_VideoConf3.png')],
                    dialog : false,
                    model: 0,
                    techUsed:'Vue.Js, Vuetify .'
                },
            ]
        }
    },

    methods: {
        
    },

}

</script>


<style scoped>
/* #projects{
  padding: 20px;
} */
.events-heading
{
    margin: 20px;
  text-align: center;
  font-size: 4em;
  font-weight: 700;
}
.v-card{
    border: none;
}
.v-card--reveal {
  align-items: center;
  bottom: 0;
  justify-content: center;
  opacity: .5;
  position: absolute;
  width: 100%;
}

</style>