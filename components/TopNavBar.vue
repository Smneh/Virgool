<template>
    <v-container>
        <v-app-bar flat color='#fff' class="my-6 px-4"> 
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
        </v-app-bar>
    </v-container>
</template>

<script>

export default {
     methods:{
         Clicked(){
             console.log("hello")
         }
     }
}
</script>

<style lang="scss" scoped>

</style>