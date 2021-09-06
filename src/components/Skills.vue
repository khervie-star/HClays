<template>
    <div style="margin-top:40px;">
        <div class="services">
            <span>Skills</span>
        </div>
        <div class="side-header text-left">Skills</div>
        <b-container class="bv-example-row">
          <!-- <b-row> -->
            <ul id="example-2">
              <b-row>
              <b-col>

                <li class="d-inline-flex" v-for="(item) in paths"  v-bind:key="item">
                    <div style="padding:10px; padding-left:0px;" class="skill text-left">
                        <!-- <mdb-btn slot="reference"> -->
                       <mdb-popover trigger="hover" :options="{placement: 'top'}">
                          <span slot="body">
                            <a-progress
                              type="circle"
                              :stroke-color="{
                              '0%': item.color,
                              '100%': item.color,
                              }"
                              :percent="item.percennt"
                              :width="75"
                            />
                          </span>
                          <b-img slot="reference" id="popover-target-1"  :src="item.icon" width="30%"/>
                        </mdb-popover>
                        <!-- </mdb-btn> -->
                      <b-card-text>
                        <span>
                          {{ item.name }}
                        </span>
                      </b-card-text>
                    </div>   
                </li>
              </b-col>
              </b-row>
            </ul>
        </b-container>
    <!-- <div>
        <a-progress
      type="circle"
      :stroke-color="{
        '0%': '#108ee9',
        '100%': '#87d068',
      }"
      :percent="90"
      :width="75"
    />
    <a-progress type="circle" :percent="70" :width="75" status="exception" />
    <a-progress type="circle" :percent="100" :width="75" />
  </div> -->
    </div>


</template>


<script>
  import { mdbPopover, mdbBtn } from 'mdbvue';


export default {
  name: 'PopoverExample',
      components: {
      mdbPopover,
      // mdbBtn
    },
    data() {
    return {
      paths: [
         {
            name: "HTML/CSS",
            icon: require("../assets/icons/pngs/html.png"),
            color: "#e44d26",
            percennt: "90",
        },
         {
            name: "BOOTSTRAP",
            icon: require("../assets/icons/pngs/bootstrap-4.png"),
            color: "#563d7c",
            percennt: "85",
        },
         {
            name: "JavaScript",
            icon: require("../assets/icons/pngs/javascript-programming-language.png"),
            color: "#f7df1e",
            percennt: "75",
        },
         {
            name: "TypeScript",
            icon: require("../assets/icons/pngs/typescript-programming-language.png"),
            color: "#007acc",
            percennt: "60",
        },
         {
            name: "ReactJs",
            icon: require("../assets/icons/pngs/react-js.png"),
            color: "#00d8ff",
            percennt: "75",
        },
         {
            name: "VueJs",
            icon: require("../assets/icons/pngs/vue-js.png"),
            color: "#4dba87",
            percennt: "70",
        },
         {
            name: "Python",
            icon: require("../assets/icons/pngs/python-programming-language.png"),
            color: "#4180b2",
            percennt: "60",
        },
         {
            name: "Linux",
            icon: require("../assets/icons/pngs/linux.png"),
            color: "#121212",
            percennt: "80",
        },
         {
            name: "Operating Systems",
            icon: require("../assets/icons/pngs/linux-ubuntu.png"),
            color: "#121212",
            percennt: "70",
        },
    ]
  }
}}
</script>


<style scoped>
  .popover{
    background-color: red !important;
  }
  .popover_arrow{
    display: none !important;
  }
  ul{
    list-style-type: none;
  }
  .skill{
      margin: 10px;
  }
  .skill span{
      opacity: 0.8;
      font-size: 0.9em;
      font-weight: 600;
      margin-bottom: -400px !important;
  }
  .services span {
    font-size: 80px;
    position: absolute;
    left: 0;
    right: 0;
    text-align: center;
    top: 52vh;
    z-index: 0;
    opacity: 0.05;
    font-weight: 700;
  }
    .side-header{
    font-size: 1.4em;
    font-weight: 700;
    position: absolute;
    right: 150px;
    bottom: 150px;
    color: #484545;
    width: 150px;
    height: 35px;
    border-bottom: 3px solid #484545;
    /* background-color: yellow; */
  -ms-transform: rotate(90deg); /* IE 9 */
  transform: rotate(90deg);
    }
.ant-progress-circle-wrap,
.ant-progress-line-wrap {
  margin-right: 8px;
  margin-bottom: 5px;
}
@media (max-width:768px) {
    .side-header{
    display: block;
    font-size: 1.4em;
    font-weight: 700;
    position: relative !important;
    right: -50px; bottom: 0px;
    color: #484545;
    width: 150px;
    height: 35px;
    border-bottom: 3px solid transparent;
    transform: none !important;
    -ms-transform: none !important; /* IE 9 */
    }
}
      @media (min-width: 991px) {
        .side-header{ 
          /* display:none !important; */
        }}
</style>