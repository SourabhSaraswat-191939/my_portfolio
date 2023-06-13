<template>
<div id="experience">
  
        <v-card class="events-heading" > Industry Experience
        </v-card>
  
  <v-timeline >
    <v-timeline-item
      v-for="(year, i) in years"
      :key="i"
      large
    >
    <template v-slot:icon>
        <v-avatar style="background-color:white;" >
          <img :src="year.company_img">
        </v-avatar>
    </template>
      <template v-slot:opposite>
        <span
          :class="`headline font-weight-light ${year.color}--text`"
          v-text="year.year"
        ></span>
      </template>
      <div class="py-4">
        <h2 :class="`headline font-weight-bold mb-4 ${year.color}--text`">
          {{year.role}}
        </h2>
        <h3>
          {{year.company}}
        </h3>
        <div v-html="year.work">
          <!-- {{year.work}} -->
        </div>
      </div>
    </v-timeline-item>
  </v-timeline>
</div>
</template>


<script>
  export default {
    data: () => ({
      years: [
      {
          color: 'green',
          year: 'Feb 2023 - Present',
          role: 'Software Development Engineer',
          company: 'GeeksForGeeks',
          company_img: require('../assets/GFG.png'),
          work: 'Working on a GeeksforGeeks practice and job portal using Django and Next.js which is used by Millions of peoples. Worked on developing features on Contest, Job Recommendation, Report Issue and on some Internal Dashboards.<br/>Conducted thorough bug analysis and successfully resolved a variety of software issues.'
        },
        {
          color: 'orange',
          year: 'Aug 2021 - Dec 2021',
          role: 'Vue.Js Mentor',
          company: 'GirlScript Winter of Contributing',
          company_img: require('../assets/GWOC.png'),
          work: 'This was a 3 months journey with GirlScript Winter of Contributing as a Mentor for Vue.Js. It was a great experience with #opensource and I must say that I learned a lot while mentoring contributors to contribute and by solving their doubts. <br/>At the end of program I was selected as one of the #Top_Mentor under FRONTEND WEB DEVELOPMENT WITH #REACT, #ANGULAR, AND #VUE  domain. Specifically, I was mentoring for #Vue.'
        },
        {
          color: 'text--accent-1 red',
          year: 'Aug 2021 - Oct 2021',
          role: 'APP DEVELOPMENT INTERN',
          company: 'Awechemist Technologies PVT. LTD',
          company_img: require('../assets/expresso.jpeg'),
          work: 'Worked on a Social Media Application named Expresso using Flutter and its popular packages. Developed the complete frontend with server integration of one of the important modules (i.e. cutesy) of the app. Worked on Models designing, building local databases, and storing data using sqflite package. Developed a Real-Time chatting feature using socket_io_client package and improved as per the user’s feedback.'
        },
        {
          color: 'green',
          year: 'Nov 2020 - Jan 2021',
          role: 'Full Stack Web Developer INTERN',
          company: 'Groocy Retails',
          company_img: require('../assets/groocy.png'),
          work: 'Working as a Web Developer Intern in Groocy RETAILS (OPC) PRIVATE LIMITED Project . Working on Fronthand to design UI, Backend and Server Deployment . As a result of this experience, I’m more excited than ever and feel more-equipped to take on Web Developer Responsibility . I loved fixing and learning from real time bugs , working for developing new functionalities.'
        },
        {
          color: 'cyan',
          year: 'Sep 2020 - Oct 2020',
          role: 'Full Stack Developer',
          company: 'Medicare Solution',
          company_img: require('../assets/medicare_solution.png'),
          work: 'It\'s a platform which i created as a Freelancer for a private Company by which they sell their medical products online .Their are multiple features including order status , online payment ,search, email verification, order tracking etc., which will be so helpfull for users .'
        },
      ],
    }),
  }
</script>

<style scoped>
#experience{
  padding: 20px;
}

.events-heading
{
  text-align: center;
  font-size: 4em;
  font-weight: 700;
}
</style>


