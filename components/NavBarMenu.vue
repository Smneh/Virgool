<template>
    <v-container fluid class="primaryBg">
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
    }
}
</script>

<style lang="scss" scoped>

.primaryBg{
    background-color: $primary-blue !important;
    color: $white;
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

