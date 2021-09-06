<template>
  <a-timeline>
    <a-timeline-item color="red"> 
      <a-icon slot="dot" type="edit" />
      <h6>
        BSc. Physics
      </h6>
      <span> University of Ibadan (2017 - Present)</span>
    </a-timeline-item>
    <a-timeline-item color="red"> 
      <a-icon slot="dot" type="edit" />
      <h6>
        High School Degree
      </h6>
      <span> American Christian Academy (2016 - 2017)</span>
    </a-timeline-item>
    <a-timeline-item>
      <a-icon  slot="dot" type="code" /> 
      <h6>
        Web Developer/Volunteer
      </h6>
      <span>
        Frontida Zois Initiative
      </span> 
    </a-timeline-item>
    <a-timeline-item color="red">
      <a-icon slot="dot" type="clock-circle-o" style="font-size: 16px;" />
      <h6>Front</h6>
      <span>Chiptranz Systems</span>
    </a-timeline-item>
    <a-timeline-item color="green"> 
      <a-icon slot="dot" type="usergroup-delete" />
      <!-- <a-icon type="code" /> -->
      <h6>
        Member
      </h6>
      <span> Developers Student Club UI (Present)</span>
    </a-timeline-item>
  </a-timeline>
</template>


<script>
export default {
  data() {
    return {
      PreviousExperiene : [
        {
          name: "Developers Student Club UI",
          role: "Member",
          text: "",
          icon: require('../assets/dsc.jpg'),
          opposite: "",
        },
         {
          name: "Frontida Zois Initiative",
          role: "Volunteer/ IT lead",
          text: "",
          icon: require('../assets/fzi.png'),
          opposite: "",
        },
         {
          name: "Chiptranz Systems",
          role: "Front-end Developer",
          text: "",
          icon: require('../assets/chiptranz.jpg'),
          opposite: "",
        },
      ]
    }
  }
}
</script>

<style>
.ant-timeline-item-head{
  background-color: transparent !important;
}
</style>