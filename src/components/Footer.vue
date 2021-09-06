<template>
  <!-- Footer -->
  <div class="footer">
    <mdb-footer color="transparent" class="font-small pt-4 mt-4" style="position: absolute; width: 100vw;">
      <div class="footer-copyright text-center py-3" style="background-color: transparent;">
        <mdb-container fluid style="color: #121212; font-size: 1em">
          &copy; 2021 Copyright: Kwesi Hervie
        </mdb-container>
      </div>
    </mdb-footer>
  </div>
  <!-- Footer -->
</template>

<script>
  import { mdbFooter, mdbContainer,} from 'mdbvue';
  export default {
    name: 'FooterPage',
    components: {
      mdbFooter,
      mdbContainer,
    }
  }
</script>

<style scoped>
ul{
  display: inline;
}
li{
  display: inline !important;
}
</style>