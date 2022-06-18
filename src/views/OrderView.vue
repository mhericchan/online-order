<template>
    

    <AppBar/>

  

    <CategoryTab />

</template>

<script>
import AppBar from '@/components/AppBar.vue';
import CategoryTab from '@/components/CategoryTab.vue';
export default {
    name: 'OrderView',
    components: {AppBar, CategoryTab},

}
</script>
<style>

</style>
