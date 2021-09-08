<template>
  <div>
    <b-container class="bv-example-row">
      <b-row>
        <b-col class="text-left" style="padding-right:50px" sm="6">
          <div class="left-header">
            <h2> Just say hi.</h2>
            <span>I'm always open to discuss your project and talk about new things.</span>
          </div>
          <div class="follows">
            <b-row>
              <b-col>
                <div >
                  <span class="pre-link">Mail me at</span><br />
                  <a href="mailto:khervie00@outllok,com">khervie00@outlook.com</a>
                </div>
              </b-col>
              <b-col>
                <div class="text-right">
                  <span class="pre-link">Follow me</span><br />
                    <div>
                      <socials />
                    </div>
                </div>
              </b-col>
            </b-row>
          </div>
        </b-col>
        <b-col sm="6">
          <div class="form">
            <ReachOutForm />
          </div>
        </b-col>
            </b-row>
        </b-container>
        <div>
          <Footer />
        </div>
  </div>
</template>

<script>
import { Component, Vue } from 'vue-property-decorator';
import Footer from "@/components/Footer.vue";
import ReachOutForm from "@/components/ReachOutForm.vue";
import Socials from '@/components/Socials.vue'


@Component({
  components: {
    Footer,
    ReachOutForm,
    Socials

  },
})

export default class Profile extends Vue {}
</script>

<style scoped>
.bv-example-row{
  margin-top: 120px !important;
}
.left-header h2{
  font-weight: bold;
  font-size: 60px;
  margin-bottom: 80px;
}
.left-header span{
  font-size: 30px;
  margin-bottom: 30px;
}
.follows{
  margin-top: 50px;
}
.pre-link{
  font-size: 1em;
  color: #121212;
  opacity: 0.4;
  margin-right: 20px;
  padding-bottom: 1 00px !important;
}
.pre-link div{
  float: right;
}
a{
  text-decoration: underline !important;
  color: inherit;
  font-weight: bold;
}
 /* @media (max-width: 575px) {
       .form{
    }
   } */

     @media (min-width: 575px) and (max-width: 768-x) { 
       .form{
      display: none !important;
    }
      }


  /* Small devices (landscape phones, less than 768px) */
  @media (max-width: 767px) { 
    .left-header h2{
      font-size: 45px;
      margin-bottom: 50px;
    }
    .left-header span{
      font-size: 20px;
      margin-bottom: 10px;
    }
    .text-right .pre-link, .text-right div{
      float: left !important;
    }
    .follows div{
      margin-bottom: 20px;
    }
   }

  /* Medium devices (tablets, less than 992px) */
  @media (max-width: 991px) { 
        .left-header h2{
      font-size: 45px;
      margin-bottom: 50px;
    }
    .left-header span{
      font-size: 20px;
      margin-bottom: 10px;
    }
    .text-right .pre-link, .text-right div{
      float: left !important;
    }
    .follows div{
      margin-bottom: 20px;
    }
   }

  /* Large devices (desktops, less than 1200px) */
  @media (max-width: 1199px) {  }
</style>
