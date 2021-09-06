<template>
    <div>
  <b-navbar toggleable="lg" type="light" variant="transparent">
    <b-navbar-brand href="#">
      <img src="../assets/Khervie00_logo.png"  width="40%"/>
    </b-navbar-brand>

    <b-navbar-toggle target="nav-collapse">
    </b-navbar-toggle>

    <b-collapse id="nav-collapse" is-nav>
      <b-navbar-nav class="ml-auto" right>
        <b-nav-item>
          <router-link to="/">Home</router-link>
        </b-nav-item>
        <b-nav-item>
          <router-link to="/profile">Profile</router-link>
        </b-nav-item>
        <b-nav-item>
          <router-link to="/experience">Qualifications</router-link>
        </b-nav-item>
         <b-nav-item>
          <router-link to="/contact">Contact</router-link>
        </b-nav-item>
      </b-navbar-nav>

      <!-- Right aligned nav items -->
    </b-collapse>
  </b-navbar>
</div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';

@Component
export default class NavBar extends Vue {}
</script>

<style scoped>
.navbar{
  box-shadow: none !important;
}
.nav-item a{ 
  color: #121212 !important;
  /* font-weight: bold; */
  font-size: 16px;
  opacity: 0.9;
  font-weight: 700;
}

.nav-item a:hover{
  text-decoration: none;
  opacity: .6;
  font-weight: 700;
}
.nav-item a:active{
  color: red;
}

</style>
