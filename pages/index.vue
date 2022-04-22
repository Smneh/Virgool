<template>
  <div>
    <header>
      <nav-bar />
    </header>
    <div class="home-page">
      <recommended-posts />       
      <promotion-box />       
    </div>
  </div>
</template>

<script>
export default {
  name: 'IndexPage',

}
</script>

<style lang="scss" scoped>
.home-page{
  background-color: $home-bg;
  padding: 80px 0;
}
</style>