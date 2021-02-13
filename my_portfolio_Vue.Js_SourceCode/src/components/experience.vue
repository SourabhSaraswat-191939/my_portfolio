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
        <v-avatar>
          <img :src="year.company_img">
        </v-avatar>
    </template>
      <template v-slot:opposite>
        <span
          :class="`headline font-weight-bold ${year.color}--text`"
          v-text="year.year"
        ></span>
      </template>
      <div class="py-4">
        <h2 :class="`headline font-weight-light mb-4 ${year.color}--text`">
          {{year.role}}
        </h2>
        <h3>
          {{year.company}}
        </h3>
        <div>
          {{year.work}}
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
          year: 'Nov 2020 - Jan 2021',
          role: 'Full Stack Web Developer',
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