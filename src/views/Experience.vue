<template>
    <div>
      <b-container class="containerr" fluid style="padding: 10px 50px;">
        <div class="text-left experience"> 
          <span >Education, </span><br /><span>Work Experience, </span><span style="font-size:17px">and </span><span>Skills</span><br />
        </div>
        <div class="text-left" style="margin-bottom:50px">
          <p style="width:60vw; color:#121212; opacity:.75;">
            Summary of my work experiences, volunteer experiences, education and projetcs done.
          </p>
        </div>
        <b-row>
          <b-col class="text-left" sm="6"> 
            <experience-timeline />    
          </b-col>
          <b-col>
            <other-skilss  sm="6"/>
          </b-col>
        </b-row>
      </b-container>
    </div>
</template>

<script>
import { Component, Vue } from 'vue-property-decorator';
import ExperienceTimeline from '@/components/ExperienceTimeline.vue'
import OtherSkilss from '@/components/OtherSkilss.vue';

@Component({
  components: {
    ExperienceTimeline,
    OtherSkilss,
  },
})

export default class Experience extends Vue {}
</script>

<style scoped>
 @media (max-width: 575px) {  
   .containerr{
     margin-top: 90px;
   }
 }
.experience{
  position: relative;
  font-weight: bold !important;
  font-size: 38px !important;
  opacity: 0.8;
}
.perks{
  position: relative;
  font-weight: bold !important;
  font-size: 40px !important;
  opacity: 0.55;
}
</style>