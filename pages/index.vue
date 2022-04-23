<template>
  <div>
    <header>
      <nav-bar />
    </header>
    <div class="home-page">
      <recommended-posts />       
      <promotion-box />
      <home-page-content />       
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
  background-color: $gray-100;
  padding: 80px 0;
}
</style>