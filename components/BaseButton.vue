<template>
    <div>
        <v-btn 
          v-on="$listeners"
          :class="buttonClass"
          v-bind="$attrs"
        >
        <slot></slot>
        </v-btn>
    </div>
</template>

<script>

export default {
  inheritAttrs: false,
  props: {
    buttonClass: {
      type: String
    }
  }
}
// export default {
//     props: {
//       rounded: {
//         type: Boolean,
//         default: false,
//       },
//       color: {
//         type: String,
//         default: null,
//       },
//       text: {
//         type: Boolean,
//         default: false,
//       },
//       outlined :{
//         type: Boolean,
//         default: false,
//       },
//       ripple :{
//         type: Boolean,
//         default: false,
//       },
//       icon :{
//         type: Boolean,
//         default: false,
//       },
//       className :{
//         type: String,
//         default: null,
//       },
//       to :{
//         type: String,
//         default: null
//       }
//     },
// }
</script>

<style lang="scss" scoped>
.v-btn{
    height: 30px !important;
    font-size: 13.3px !important;
    padding: 5px 25px !important;
   &::before{
      background-color: transparent !important;
   }   
}

.primaryBtn{
    background-color: $primary-blue;
    color : $white !important;
}

.lightBtn {
  background-color: $white;
  color :  $primary-blue !important;
}
</style>