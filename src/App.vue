<template>
  <div id="app">
    <!-- <nav-bar /> -->
    <!-- <router-view /> -->
    <falling-leaves />
    <full-page-view />
  </div>
</template>

<script>
import { Component, Vue, } from 'vue-property-decorator';
import NavBar from '@/components/NavBar'
import FallingLeaves from "@/components/LeafFall.vue"
import FullPageView from "@/FullPageView.vue"

@Component({
  components: {
    NavBar,
    FallingLeaves,
    FullPageView,

  }
})

export default class App extends Vue {}
</script>

<style lang="scss">
@font-face {
  font-family: 'Rubik';
  src: url('./fonts/Rubik/Rubik-VariableFont_wght.ttf') format("truetype");
}
#app {
  font-family: "Rubik", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #121212 !important;
  background-color: #f8f8f8 !important;
  height: 100vh;
  // overflow: hidden;
}

#nav {
  padding: 30px;

  a {
    font-weight: bold;
    color: #2c3e50;

    &.router-link-exact-active {
      color: #42b983;
    }
  }
}
</style>