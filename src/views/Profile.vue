<template>
    <div id="profile">
        <v-divider
          class="mx-4"
          vertical
        ></v-divider>
        <About />
         <v-divider vertical></v-divider>
          <a-divider type="vertical" />
        <Skills />
    </div>
</template>

<script>
import { Component, Vue } from 'vue-property-decorator';
import 'ant-design-vue/dist/antd.css';
import Skills from "@/components/Skills.vue";
import About from "@/components/About.vue";

@Component({
  components: {
    Skills,
    About

  },
})

export default class Profile extends Vue {}
</script>

<style scoped>
#profile{
  /* margin-top:100px; */
}
 @media (max-width: 575px) {  }

  /* Small devices (landscape phones, less than 768px) */
  @media (max-width: 767px) {  
    #profile{
      overflow: visible !important;
      margin-top:100px;
    }
  }

  /* Medium devices (tablets, less than 992px) */
  @media (max-width: 991px) {  }

  /* Large devices (desktops, less than 1200px) */
  @media (max-width: 1199px) {  }
</style>