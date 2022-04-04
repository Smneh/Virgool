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

<style >
@import url('https://v1.fontapi.ir/css/Vazir');

.v-application {
  font-family: Vazirmatn, sans-serif !important;
}

.content-container {
    max-width: 1000px !important;
    padding-left: 16px !important;
    padding-right: 16px !important;
}
</style>
