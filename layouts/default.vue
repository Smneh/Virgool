<template>
  <v-app >
    <v-main>
        <Nuxt />
    </v-main>
  </v-app>
</template>

<script>
export default {
  name: 'DefaultLayout',
}
</script>

<style lang="scss">
@import url('https://v1.fontapi.ir/css/Vazir');

.theme--light {
  &.v-application {
    font-family: Vazirmatn, sans-serif !important;
    line-height: 2 !important;
    direction: rtl;
    word-wrap: break-word;
    background-color: $white;
    color: $text-color;
    font-size: 16px;
    font-weight: 400;
    letter-spacing: 0;
  }
}

.content-container {
  width: 100%;
  margin: 0 auto;
  max-width: 1000px !important;
  padding: 0 16px !important;
}

.section-subtitle{
    color: $light-gray;
    font-family: inherit;
    font-size: 12.8px;
}

.section-body {
    display: flex;
    flex-wrap: wrap;
}

.row{
  margin: 0 !important;
}

</style>
