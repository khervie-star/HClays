<template>
  <div class="about">
    <b-container>
      <div class="services">
        <span>Services</span>
      </div>
      <div>
        <div class="side-header text-right">What I Do</div>
         <b-row>
            <ul id="example-2" style="">
                <b-col>
                <li class="d-inline-flex" v-for="(item) in paths"  v-bind:key="item">
                  <div>
                    <b-img id="popover-target-1"  :src="item.icon" width="70%"/>
                    <b-card
                      :title="item.name"
                      img-alt="Image"
                      img-top
                      tag="article"
                      style="max-width: 20rem;"
                      class="mb-2"
                    >
                      <b-card-text>
                        {{ item.text }}
                      </b-card-text>
                    </b-card>
                  </div>     
                </li>
              </b-col>
            </ul>
          </b-row>
      </div>
    </b-container>
  </div>    
</template>

<script>
import Vue from 'vue';

export default {
    data() {
    return {
      paths: [
         {
            name: "Web Development",
            text: "Intermediate level web developer with vast knowledge and usage of JavaScript and JavaScript frameworks to build SWAs and PWAs to a standard scale ..",
            icon: require("../assets/icons/pngs/full-stack-developer.png"),
        },
         {
            name: "Design",
            text: "Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua Ut enim...",
            icon: require("../assets/icons/pngs/full-stack-developer.png"),
        },
         {
            name: "Embedded Systems",
            text: "Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua Ut enim...",
            icon: require("../assets/icons/svg/iot.svg"),
        },
    ]
  }
}}
</script>

<style scoped>
  .mb-2{
    background-color: transparent !important;
    box-shadow: none;
    border: none;
  }

  .services span {
    font-size: 100px;
    position: absolute;
    left: 0;
    right: 0;
    text-align: center;
    top: 50px;
    z-index: 0;
    opacity: 0.05;
    font-weight: 700;
  }
  .services h3{
    position: relative;
    margin-bottom: 50px;
    /* font-weight: bold; */
  }
  .about{
    margin-top: 40px;
  }
  .side-header{
    font-size: 1.4em;
    font-weight: 700;
    position: absolute;
    left: 100px;
    top: 250px;
    color: #484545;
    width: 150px;
    height: 35px;
    border-bottom: 3px solid #484545;
    /* background-color: yellow; */
  -ms-transform: rotate(270deg); /* IE 9 */
  transform: rotate(270deg);
    }
      @media (max-width: 991px) {
        .side-header{ 
          display:none !important;
        }
      }
</style>