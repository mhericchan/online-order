<template>
  <v-card height="100%">
    <v-tabs v-model="tab" dark color="cyan" centered center-active show-arrows hide-slider="true" hide-controls>
      <v-tab v-for="item in categorys" :key="item.type" :value="item.type">{{
        item.type
      }}</v-tab>
    </v-tabs>
    <v-container>
      <v-window v-model="tab">
        <v-window-item v-for="item in categorys" :key="item.type" :value="item.type">
          <v-row  style="margin-top:5px !important">
            <v-col cols="12" v-for="(foodName, i) in item.menu" :key="i"
              ><v-card class="dishes_size" elevation="3" outlined height="100%" 
                ><v-row
                  ><v-col cols="8" style="padding-right: 0px !important"
                    ><v-card-title>{{ foodName }}</v-card-title
                    ><v-card-subtitle><r-row><div v-for="(desc, index) in item.description[i]" :key="index">{{ desc }}</div></r-row></v-card-subtitle
                    ><v-card-text style="font-size: 4sp !important">
                      HK$ {{ item.price[i] }}</v-card-text
                    >
                  </v-col>
                  <v-col cols="4" style="padding-left: 0px !important"
                    ><v-img
                      aspect-ratio="1"
                      height="90%"
                      width="auto"
                      style="width: auto; margin-right: 10px"
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
          menu: ["二人餐", "二人大餐", "	啖啖肉(大批)-買一送一"],
          price: [198, 40, 50],
          description: [
            ["指定三藩市式手藝薄批/鬆厚批/薄脆批(普通批) x 1", "指定意粉/飯/小食 x 1", "百事可樂(罐) x 2"],
            ["指定三藩市式手藝薄批/鬆厚批/薄脆批(大批) x 1", "指定飯/意粉/小食 x 1",  "指定小食 x 1", "百事可樂(罐) x 2"],
            ["指定三藩市式手藝薄批/鬆厚批/薄脆批(大批) x 2", "正價購買任何大批，買一送一",  "（公眾假期除外）"],
          ],
          src: [
            "https://51wm-pic1.oss-accelerate.aliyuncs.com/product/04370aaf-783b-48e9-8db2-d45be3d41e92.png",
            "https://51wm-pic1.oss-accelerate.aliyuncs.com/product/5e6f4913-707d-400e-a646-896a4bd4009f.png",
            "https://51wm-pic1.oss-accelerate.aliyuncs.com/product/d3107c49-aee1-45f2-a849-0477db4b6c97.png",
          ],
        },
        { 
          type: "rice", 
          menu: ["白飯", "揚州炒飯"],
          price: [10, 20],
           description: [
            ["白飯 x 1"],
            ["揚州炒飯 x 1", "飲品(涷飲) x 1"],
          ],
          src: [
            "https://51wm-pic1.oss-accelerate.aliyuncs.com/product/04370aaf-783b-48e9-8db2-d45be3d41e92.png",
            "https://51wm-pic1.oss-accelerate.aliyuncs.com/product/5e6f4913-707d-400e-a646-896a4bd4009f.png",
            
          ],
        },
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
*{
  -moz-user-select: none; -webkit-user-select: none; -ms-user-select:none; user-select:none;-o-user-select:none;
}
</style>
