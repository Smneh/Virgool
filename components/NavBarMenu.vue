<template>
    <v-container fluid class="primaryBg" :class="{'fixed-menu' : fixed }">
        <v-container class="content-container">
            <v-row> 
                <ul>
                    <li v-for="(item , index) in items" :key="index" >{{ item }}</li>
                </ul>
                </v-row>
        </v-container>
    </v-container>
</template>

<script>
export default {
        data () {
            return {
                fixed:false,
                items: [
                    'جدید ترین پست ها',
                    'پست های دوستان',
                    'استارتاپ',
                    'کسب و کار',
                    'موفقیت',
                    'خلاقیت',
                    'برنامه نویسی',
                    'طنز',
                    'حال خوبتو با من تقسیم کن'
                ]
            }
    },
    methods:{
        setPositionFix(){
            this.fixed = true
        },
        removePositionFix(){
            this.fixed = false
        }
    }
}
</script>

<style lang="scss" scoped>

.primaryBg{
    background-color: $primary-blue !important;
    color: $white;
    top: 100px;
    position: absolute;
    transition:top 0.5s linear;
}

.fixed-menu{
    position: fixed;
    right: 0;
    top: 0;
    width: 100%;
    z-index: 99;
    transition:top 0s linear;
}

ul {
    list-style-type: none;
    display: flex;
    gap: 20px;
    flex-direction: row-reverse;
    font-size: 12.5px;
    margin-left: auto;
    padding: 8px 0;

    li{
        opacity: 0.64;
        cursor: pointer;
        transition: opacity 0.3s ease-in-out;

        &:hover,
        &:nth-child(1),
        &:nth-child(2){
            opacity: 0.84;
        }
    }
}

</style>

