<template>
  <v-app>
    <Navbar/>
    
    <v-main>
      <router-view/>
    </v-main>

    <bottomNavbar />
  </v-app>
</template>

<script>

import Navbar from './components/Navbar.vue'
import bottomNavbar from './components/bottomNavbar.vue';
export default {
  name: 'App',

  data: () => ({
    //
  }),

  components : {
    Navbar,
    bottomNavbar
  }
};
</script>

<style>
@import url('@/assets/styles.css');
</style>
