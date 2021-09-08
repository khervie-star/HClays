<template>
  <div>
    <a-timeline>
      <a-timeline-item color="red"> 
        <a-icon slot="dot" type="edit" />
        <h6>
          BSc. Physics
        </h6>
        <span> University of Ibadan   </span>
      </a-timeline-item>
      <!-- <a-timeline-item color="green"> 
        <a-icon slot="dot" type="edit" />
        <h6>
          High School Degree
        </h6>
        <span> University of Ibadan University of Ibadan</span>
      </a-timeline-item> -->
      <a-timeline-item color="blue">
        <a-icon  slot="dot" type="code" /> 
        <h6>
          Web Developer/Volunteer
        </h6>
        <span>
          University of Ibadan University of Ibadan 
        </span> 
      </a-timeline-item>
      <a-timeline-item color="red">
        <a-icon slot="dot" type="clock-circle-o"/>
        <h6>Frontend role</h6>
        <span>Chiptranz Systems (Present) </span>
      </a-timeline-item>
      <a-timeline-item color="green"> 
        <a-icon slot="dot" type="usergroup-delete" />
        <h6>
          Member
        </h6>
        <span> Developers Student Club UI (Present)</span>
      </a-timeline-item>
    </a-timeline>
  </div>
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
.ant-timeline-item{
  display: flex !important;
  flex-direction: column !important;
}
</style>