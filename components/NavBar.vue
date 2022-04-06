<template>
   <v-container fluid class="pa-0 main-navbar" >
      <top-nav-bar @top-nav-is-out="fixMenu" @top-nav-is-in='unfixMenu' ></top-nav-bar>
      <nav-bar-menu ref="menu"></nav-bar-menu>
   </v-container>
</template>

<script>


export default {
   methods:{
      fixMenu(){
         this.$refs.menu.setPositionFix()
      },
      unfixMenu(){
         this.$refs.menu.removePositionFix()
      }
   }
}
</script>

<style lang="scss" scoped>

</style>