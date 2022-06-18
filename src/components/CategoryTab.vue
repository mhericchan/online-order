<template>
  <v-card height="100%">
    <v-tabs v-model="tab" dark color="blue" centered center-active show-arrows>
      <v-tabs-slider color="teal lighten-3"></v-tabs-slider>
      <v-tab v-for="item in categorys" :key="item.type" :value="item.type">{{
        item.type
      }}</v-tab>
    </v-tabs>
    <v-container>
      <v-window v-model="tab">
        <v-window-item v-for="item in categorys" :key="item.type" :value="item.type">
          <v-row>
            <v-col cols="12" v-for="(menu, i) in item.menu" :key="i"
              ><v-card class="dishes_size" elevation="4" outlined height="100%"
                ><v-row
                  ><v-col cols="8" style="padding-right: 0px !important"
                    ><v-card-title>{{ menu }}</v-card-title
                    ><v-card-subtitle>{{ item.description[i] }}</v-card-subtitle
                    ><v-card-text style="font-size: 4sp !important">
                      HK$ {{ item.price[i] }}</v-card-text
                    >
                  </v-col>
                  <v-col cols="4" style="padding-left: 0px !important"
                    ><v-img
                      aspect-ratio="1"
                      height="90%"
                      width="auto"
                      style="width:auto;margin-right: 10px;"
                      :src="item.src[i]"
                    ></v-img></v-col
                ></v-row> </v-card
            ></v-col>
          </v-row>
        </v-window-item>
      </v-window>
    </v-container>
  </v-card>
</template>

<script lang="ts">
export default {
  name: "CategoryTab",

  data() {
    return {
      foodType: null,
      categorys: [
        {
          type: "Pizza",
          menu: ["二人餐", "二人大餐", "2"],
          price: [198, 40, 50],
          description: [
            "指定三藩市式手藝薄批/鬆厚批/薄脆批(普通批) X 1 /n指定意粉/飯/小食 X 1<br />百事可樂(罐) X 2",
            "指定三藩市式手藝薄批/鬆厚批/薄脆批(大批) X 1 指定飯/意粉/小食 X 1 指定小食 X 1 百事可樂(罐) X 2",
          ],
          src: [
            "https://51wm-pic1.oss-accelerate.aliyuncs.com/product/04370aaf-783b-48e9-8db2-d45be3d41e92.png",
            "https://51wm-pic1.oss-accelerate.aliyuncs.com/product/5e6f4913-707d-400e-a646-896a4bd4009f.png",
          ],
        },
        { type: "rice", menu: ["BIG2", "SMALL2"], price: [10, 20] },
      ],
      tab: null,
    };
  },
};
</script>
<style>
v-tab {
  color: white;
  background-color: orange !important;
}
.dishes_size {
  height: 150px;
  margin: 5px;
}
</style>
