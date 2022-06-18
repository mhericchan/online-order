<template>
  <v-app>
    <v-main style="height:100%">
      <router-view/>
    </v-main>
  </v-app>
</template>

<script lang="ts">
import { defineComponent } from 'vue'
import "@fontsource/noto-sans-hk";

export default defineComponent({
  name: 'App',
  data () {
    return {
      //
    }
  },
})
</script>

<style>
@import url('https://fonts.googleapis.com/css?family=Poppins');
body {
  font-family: 'Poppins';
  font-weight: 900 !important;
}
</style>