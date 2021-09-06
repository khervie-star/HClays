<template>
    <div>
        <div class="skill-progress">
            <div style="width:150px; height:150px; padding:6px;">
                <div style="width:130px; height:130px; padding:6px;"> 
                    <div style="width:110px; height:110px">    
                    </div>
                </div>
            </div>
        </div>

        <div class="progress-bars">
            <a-progress type="circle" :percent="30" :width="80" status="active" />
            <a-progress type="circle" :percent="70" :width="85" status="active"/>
            <a-progress type="circle" :percent="100" :width="90" active/>
        </div>
    </div>
</template>

  <!-- <div>
    <a-progress type="circle" :percent="75" :format="percent => `${percent} Days`" />
    <a-progress type="circle" :percent="100" :format="() => 'Done'" />
    <a-progress type="circle" :percent="75">
      <template #format="percent">
        <span style="color: red">{{ percent }}</span>
      </template>
    </a-progress>
  </div> -->


<script>
export default {
    
}
</script>

<style scoped>
    .skill-progress{
        align-content: center;
        text-align: center;
        align-items: center;
    }
    .skill-progress div{
        position: absolute;
        border: 3px solid grey;
        border-radius: 50%;
    }
    .skill-progress div:nth-child(2n){
        border-color: red;
    }
    .some-other-skills div{
        position: absolute;
        border: 5px solid grey;
        border-radius: 50%;
    }
    .progress-bars{
        position: absolute;
    }
    div.ant-progress-circle,
    div.ant-progress-line {
    margin-right: 8px;
    margin-bottom: 8px;
    }
</style>