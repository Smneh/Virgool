<template>
    <div fluid class="primaryBg" :class="{'fixed-menu' : fixed }">
        <div class="content-container py-3">
            <ul>
                <li v-for="(item , index) in items" :key="index" >{{ item }}</li>
            </ul>
        </div>
    </div>
</template>

<script>
export default {
        data () {
            return {
                fixed:false,
                items: [
                    'جدیدترین پست ها',
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
    background-color: $color-blue !important;
    color: $white;
    top: 100px;
    position: absolute;
    transition:top 0.5s linear;
    width: 100%;
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
    font-size: 12px;
    font-weight: 300;
    letter-spacing: 0;
    margin-left: auto;

    li{
        opacity: 0.6;
        cursor: pointer;
        transition: opacity 0.3s ease-in-out;

        &:hover,
        &:nth-child(1),
        &:nth-child(2){
            opacity: 0.9;
        }
    }
}

</style>

