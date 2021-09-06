<template>
    <div>
        <b-container class="bv-example-row">
            <b-row>
                <b-col sm="12" md="8" class="text-left">
                    <div class="bio">
                        <span style="opacity:0.8; font-size:20px;">Hello, I am</span> <span class="name">Kwesi Hervie</span>
                        <p>a <span class="sub-bio">Junior web developer</span>, <span class="sub-bio">Freelancer</span> and <span class="sub-bio"> IOT enthusiast.</span></p>
                        <p style="opacity: 0.65">I am a budding developer with proper knowledge in JavaScript and other JavaScript frameworks. With that I build responsive and scalable websites and apllications to client satisfaction.</p>
                    </div>
                    <div>
                        <b-button class="get-resume" variant="outline-primary" >Download Resume <b-icon-download /></b-button>
                    </div>
                </b-col>
                <b-col></b-col>
                <b-col md="2">
                <div>
                    <img class="logo" alt="Vue logo" src="../assets/Khervie_dev.jpg" width="100%">
                </div>
                </b-col>
                <div class="home-contact">
                    <div class="socials text-left">
                    <Socials />
                    </div>
                    <div class="email text-right">
                        <a href="mailto:khervie00@outlook.com">khervie00@outlook.com</a>
                    </div>
                </div>
            </b-row>
        </b-container>
    </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';
import Socials from '@/components/Socials.vue'

@Component({
  components: {
    Socials,
  },
})

export default class HeaderBody extends Vue {}
</script>

<style lang="scss" scoped>
.bv-example-row{
    margin-top: 50px;
}
.sub-bio{
    font-weight: bold;
    font-size: 20px;
    opacity: 0.876;
}
.socials{
    left: 150px;
    position: absolute;
    bottom: 100px;
}
.email{
    right: 150px ;
    position: absolute;
    bottom: 100px;
}
.email a{
    color: #121212 !important;
    opacity: 0.6;
    font-weight: bold;
}
.get-resume{
    border-color:#121212 !important; 
    color: inherit !important;
    margin-left: 0px !important;
}
.name{
    font-weight: bold; 
    font-size: 50px;
}

  /* Extra small devices (portrait phones, less than 576px) */
 @media (max-width: 575px) { 
     .bv-example-row{
        margin-top: -50px !important;
    }
    .socials{
        margin-left: -40px;
    }
  }
@media (min-width:568px) and (max-width:767px) {
    .socials{
        margin-left: 10vw;
    }
}
  /* Small devices (landscape phones, less than 768px) */
  @media (max-width: 767px) {
      .logo{
          display:none;
      }
      .socials{
            left: 10vw;
            position: absolute;
            bottom: 20px;
     }   
     .email{
        display: none;
     }
     .name{
         font-size: 35px;
     }
     .get-resume{
         width:200px;
         font-size: 0.8em;
     }
    }

  /* Medium devices (tablets, less than 992px) */
  @media (max-width: 991px) { 
     .logo{
          display:none;
      }
    .bv-example-row{
        //  margin-top: 50px;
    }   
    .socials, .email{
        bottom: 50px;
    }
    .socials{
        bottom:30px;
        left: 50px;
    }
}

  /* Large devices (desktops, less than 1200px) */
  @media (max-width: 1199px) { 
          .socials, .email{
        bottom: 50px;
    }
    .socials{
        bottom:30px;
        left: 50px;
    }
   }
</style>