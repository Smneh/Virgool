<template>
   <div class="main-navbar" >
      <top-nav-bar @top-nav-is-out="fixMenu" @top-nav-is-in='unfixMenu' ></top-nav-bar>
      <nav-bar-menu ref="menu"></nav-bar-menu>
   </div>
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
.main-navbar{
   width: 100%;
}
</style>