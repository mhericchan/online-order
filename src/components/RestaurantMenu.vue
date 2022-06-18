<template>
  <div>
    <v-container fluid>
      <v-row dense>
        <template v-for="(item, index) in menu" :key="index">
          <v-col cols="6" v-if="item.Type == category">
            <v-card class="mx-auto">
              <!-- <v-img
              :src="card.src"
              class="white--text align-end"
              gradient="to bottom, rgba(0,0,0,.1), rgba(0,0,0,.5)"
              height="200px"
            >
              <v-card-title v-text="123"></v-card-title>
            </v-img> -->
              {{ item.Name }} - {{ item.Price }}
              <v-card-actions>
                <v-spacer></v-spacer>

                <v-btn icon>
                  <v-icon>mdi-heart</v-icon>
                </v-btn>

                <v-btn icon>
                  <v-icon>mdi-bookmark</v-icon>
                </v-btn>

                <v-btn icon>
                  <v-icon>mdi-share-variant</v-icon>
                </v-btn>
              </v-card-actions>
            </v-card>
          </v-col>
          </template>
      </v-row>
    </v-container>
  </div>
</template>

<script lang="ts">
import Vue from "vue";
export default {
  name: "RestaurantMenu",
  props: ["category"],
  data() {
    return {
      menu: [
        { Type: "Pizza", Name: "Big Pizza", Price: 120 },
        { Type: "Pizza", Name: "Small Pizza", Price: 170 },
        { Type: "Rice", Name: "Mushroom Rice", Price: 30 },
        { Type: "Rice", Name: "Normal Rice", Price: 40 },
      ],
    };
  },
};
</script>
