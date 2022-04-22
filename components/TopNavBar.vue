<template>
    <div class="content-container py-6" :class="[ isOut ? 'hidden' : 'show' ]">
        <div 
            class="top-navbar"
            v-intersect="{
            handler: onIntersect,
            options: {threshold: [0, 0.5, 1.0]}
            }"
        >
            <base-button @click="Clicked" text buttonClass='light-btn' :ripple=false>
                <virgool-icon/>
            </base-button>

            <base-button @click="Clicked" text buttonClass='light-btn mr-3' :ripple=false >
                ویرگول چیست؟
            </base-button>

            <v-spacer />

            <base-button @click="Clicked" icon :ripple=false text color='rgb(142, 142, 142)'>
                    <v-icon >
                        mdi-magnify
                    </v-icon>
            </base-button>

            <base-button @click="Clicked" text buttonClass='light-btn mx-5' :ripple=false>
                ورود
            </base-button>

            <base-button @click="Clicked" text buttonClass='primary-btn px-6 py-1' :ripple=false to=/register >
                ثبت نام
            </base-button>
        </div>    
    </div>
</template>

<script>

export default {
    data () {
        return {
            isOut : false,
        }
    },
    methods: {
        onIntersect (entries, observer) {    
            if(entries[0].intersectionRatio >= 0.5){
                this.isOut = false
                this.$emit('top-nav-is-in')
            }else{
                this.isOut = true
                this.$emit('top-nav-is-out')
            }
        },
        Clicked(){
                console.log("hello")
        }
    }
}
</script>

<style lang="scss" scoped>
.hidden{
  transform: translateY(-50%);
  opacity: 0;
}

.show{
  transform: translateY(0);
  opacity: 1;
  transition: transform 0.5s, opacity 0.55s linear;
}

.top-navbar{
    display: flex;
    align-items: center;
    justify-content: center;
}
</style>