<template><center>
  <v-app-bar app elevation="4" color="black"
    ><v-btn icon router-link to="/"><v-icon>mdi-chevron-left</v-icon></v-btn
    ><v-app-bar-title>Pizza 外賣</v-app-bar-title
    ><v-btn icon router-link to="/"><v-icon>mdi-cart</v-icon></v-btn></v-app-bar
  ></center>
</template>
<script>
export default {
  name: "AppBar",
};
</script>
<style>
.v-toolbar.v-toolbar--flat.v-toolbar--density-default.v-toolbar--rounded.v-theme--light.v-app-bar {
  background-color: CornflowerBlue !important;
  padding: 0;
  /* text-align: center; */
}
div.v-toolbar-title.v-app-bar-title {
  /* text-align: center !important; */
}
.v-toolbar-title__placeholder {
text-overflow: clip;
}
</style>
