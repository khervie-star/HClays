<template>
    <div>
      <b-container fluid style="padding: 10px 50px;">
        <div class="text-left experience" > 
          <span >Education, </span><br /><span>Work Experience, </span><span style="font-size: 20px">and </span><span>Skills</span><br />
        </div>
        <div class="text-left">
          <p style="width:60vw;">
            Lorem ipsum dolor sit, amet consectetur adipisicing elit. Dicta veniam placeat debitis excepturi maxime itaque reiciendis praesentium quam, suscipit temporibus ipsa, dolor nobis repellendus ullam et ea ut! Mollitia, exercitationem?
          </p>
        </div>
        <b-row>
          <b-col class="text-left" cols="4"> 
            <experience-timeline />    
          </b-col>
          <b-col>
            <other-skilss  />
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
.experience{
  position: relative;
  font-weight: bold !important;
  font-size: 50px !important;
  opacity: 0.8;
}
.perks{
  position: relative;
  font-weight: bold !important;
  font-size: 40px !important;
  opacity: 0.55;
}
</style>