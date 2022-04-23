<template>
    <div>
        <v-btn 
          v-on="$listeners"
          :class="buttonClass"
          :ripple="ripple"
          :block="block"
          :loading="loading"
          :depressed="depressed"
          :disabled="disabled"
          :exact="exact"
          :fab="fab"
          :fixed="fixed"
          :outlined="outlined"
          :plain="plain"
          :retain-focus-on-click="retainFocusOnClick"
          :small="small"
          :large="large"
          :text="text"
          :type="type"
          :height="height"
          :max-height="maxHeight"
          :min-width="10"
          :width="width"
          :max-width="maxWidth"
          :to="to"
          :href="href"
          :color="color"
          :value="value"
        >
          <slot/>
        </v-btn>
    </div>
</template>

<script>
export default {
    props: {
      buttonClass: {
        type: String
      },
      color: {
        type: String,
        default: null,
      },
      text: {
        type: Boolean,
        default: false,
      },
      outlined :{
        type: Boolean,
        default: false,
      },
      ripple :{
        type: Boolean,
        default: false,
      },
      icon :{
        type: Boolean,
        default: false,
      },
      block: {
        type: Boolean,
        default: false
      },
      loading: {
        type: Boolean,
        default: false
      },
      depressed: {
          type: Boolean,
          default: false
      },
      disabled: {
        type: Boolean,
        default: false
      },
      fab: {
        type: Boolean,
        default: false
      },
      exact: {
        type: Boolean,
        default: false
      },
      fixed: {
        type: Boolean,
        default: false
      },
      small: {
        type: Boolean,
        default: false
      },
      large: {
        type: Boolean,
        default: false
      },
      retainFocusOnClick: {
        type: Boolean,
        default: false
      },
      plain: {
        type: Boolean,
        default: false
      },
      type: {
        type: String,
        default: 'button'
      },
      height: [Number, String],
      maxHeight: [Number, String],
      width: [Number, String],
      maxWidth: [Number, String],
      to: [Object, String],
      href: [Object, String],
      value: null
    },
}
</script>

<style lang="scss" scoped>
.v-btn{
  font-size: 12px !important;
  font-weight: 400 !important;
  border: 1px solid transparent;
  box-shadow: none;
  height: max-content !important;
  padding: 0 !important;
  transition: all .1s ease-in;

  &::before{
    background-color: transparent !important;
  }   
}

.primary-btn{
  background-color: $color-blue;
  color : $white !important;
}

.light-btn {
  background-color: $white;
  color :  $color-blue !important;
  
  &:hover{
    color: $dark-blue-text !important;
  }
}

.gray-btn{
  color: $gray-600 !important;
}

.start-btn{
  &:hover{
    background-color: $dark-blue-bg;
  }
}

.like-btn{
  &:hover{
    color: $red-100 !important;
  }
}

.v-btn--outlined {
  border: thin solid #5b5b5b;
  font-weight: 600 !important;
  color: $light-gray-2 !important;

  &:hover{
    border-color: $dark-text-color;
    color: $dark-text-color !important;
  }
}
</style>