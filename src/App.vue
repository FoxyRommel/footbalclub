<template>
  <MenuTop/> 
  <router-view/>
  <MenuBottom/>
</template>

<script>

  import MenuTop from "@/components/templates/MenuTop.vue";
  import MenuBottom from "@/components/templates/MenuBottom.vue";
  export default{
    components:{
      MenuTop,
      MenuBottom
    }
  }

</script>

<style>
</style>
