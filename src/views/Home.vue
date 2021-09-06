<template>
  <div>
    <header-body />
  </div>
</template>

<script lang="ts">
  import Vue from 'vue'
  import HeaderBody from '@/components/HeaderBody.vue'

  export default Vue.extend({
    name: 'Home',

    components: {
      HeaderBody,
    },
  })
</script>
