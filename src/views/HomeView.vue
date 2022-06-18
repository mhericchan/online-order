<template>
  <div class="home">
    <router-link to="/order"><button class="btn"> 按這裏開始點餐 </button></router-link>
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';


export default defineComponent({
  name: 'HomeView',
});
</script>

<style>
.home{
  height: 100%;
  width: 100%;
  background: url("https://assets.publishing.service.gov.uk/government/uploads/system/uploads/image_data/file/108320/s300_pizza-slice.jpg");
  background-repeat: no-repeat;
  background-size: cover;


}
.home:after{
  height: 100%;
  width: 100%;
  background: url("https://assets.publishing.service.gov.uk/government/uploads/system/uploads/image_data/file/108320/s300_pizza-slice.jpg");
  background-repeat: no-repeat;
  background-size: cover;
  background: rgba(0,0,0,0.1);
}

button.btn{
  position: relative;
  margin-top:30%;
  font-size: 30px;
  text-shadow: 2px 2px rgb(0,0,0);
  color: white;
  border-radius: 7px;
  padding: 20px;
  padding-left: 50px;
  padding-right: 50px;
  border: 1px solid orange;
  background-color: rgba(255, 193, 7, 0.6) ;
  box-shadow: rgba(205, 244, 244, 0.8) 0 0 2px;
}
</style>