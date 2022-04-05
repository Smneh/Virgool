<template>
    <v-container class="content-container" :class="{ 'hidden': isOut }">
        <div v-waypoint="{ active: true, callback: onWaypoint, options: intersectionOptions }">
            <v-row class="my-6"> 
                <base-button @click="Clicked" text buttonClass='primaryBtn' :ripple=false to=/register>
                    ثبت نام
                </base-button>

                    <base-button @click="Clicked" text buttonClass='lightBtn' :ripple=false>
                    ورود
                </base-button>

                    <base-button @click="Clicked" icon :ripple=false>
                        <v-icon >
                            mdi-magnify
                        </v-icon>
                </base-button>

                <v-spacer />

                <base-button @click="Clicked" text buttonClass='lightBtn' :ripple=false>
                    ویرگول چیست؟
                </base-button>

                <base-button @click="Clicked" text buttonClass='lightBtn' :ripple=false>
                    <v-img
                        lazy-src="../assets/o6jn5na3u4aw.jpeg"
                        max-height="300"
                        max-width="219"
                        src="../assets/o6jn5na3u4aw.jpeg"
                    ></v-img>
                </base-button>
            </v-row>
        </div>    
    </v-container>
</template>

<script>

export default {
    data () {
        return {
            isOut : false,
            intersectionOptions: {
                root: null,
                rootMargin: '0px 0px 0px 0px',
                threshold: [0, 1], 
            },
            } // https://developer.mozilla.org/en-US/docs/Web/API/Intersection_Observer_API
        },
    methods: {
        onWaypoint ({ going, direction }) {
        if (going === this.$waypointMap.GOING_IN && direction === this.$waypointMap.DIRECTION_TOP) {
            this.isOut = true
        }
        if (going === this.$waypointMap.GOING_OUT && direction === this.$waypointMap.DIRECTION_BOTTOM) {
            this.isOut = false
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
    display: none;
}
</style>