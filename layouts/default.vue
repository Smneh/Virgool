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

<style scoped>
@import url('https://v1.fontapi.ir/css/Vazir');

.v-application {
  font-family: Vazirmatn, sans-serif;
}
.container {
    max-width: 1000px !important;
}
</style>
