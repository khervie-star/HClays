<template>
  <!-- Material form contact -->
  <form>
    <!-- <p class="h4 text-center mb-4">Write to us</p> -->
    <div class="grey-text">
      <mdb-input label="Name" group type="text" validate error="wrong" success="right"/>
      <mdb-input label="Email" group type="email" validate error="wrong" success="right"/>
      <mdb-input label="Subject"  group type="text" validate error="wrong" success="right"/>
      <mdb-textarea :rows="2" label="Details" />
    </div>
    <div class="text-right">
      <mdb-btn class="reach_out" outline="secondary">Send <mdb-icon far icon="paper-plane" class="ml-1"/><b-icon-chevron-double-right /></mdb-btn>
    </div>
  </form>
  <!-- Material form contact -->
</template>

<script>
  import { mdbInput, mdbBtn, mdbTextarea } from 'mdbvue';
  export default {
    name: 'Basic',
    components: {
      mdbInput,
      mdbBtn,
      mdbTextarea
    }
  }
</script>

<style scoped>
form{
  background-color: #121212;
  color: #f8f8f8;
  padding: 30px;
}

.md-form label{
  color: red !important;
}

.reach_out{
  background: #f8f8f8 !important;
  border: 1px solid transparent !important;
  border-radius: 0px !important;
  justify-content: flex-end !important;
  color: #121212 !important;
}
</style>