<template>
    <v-tabs
      dark
      color="blue"
       centered center-active show-arrows
    >
      <v-tabs-slider color="teal lighten-3"></v-tabs-slider>
      <div v-for="(item, i) in category" :key="i">
        <v-tab exact-active-class="category-selected"> {{ item }}</v-tab>
      </div>
    </v-tabs>
</template>
<script>
export default {
  name: "CategoryTab",
  data() {
    return {
      category: ["Pizza", "Rice", "Pasta", "Drink"],
    };
  },
};
</script>
<style>
v-tab{
    color: white;
    background-color:orange !important;
}

</style>