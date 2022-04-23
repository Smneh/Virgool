<template>
    <div class="posts-container">
        <post-card v-for="(post,index) in posts" :key="index" :post="post" />
    </div>
</template>

<script>
export default {
    data(){
        return{
            posts :[
                {
                    title:'موضوع1',
                    authorImageSrc:'',
                    authorName:'1نویسنده',
                    date:'تاریخ1',
                    timeToRead:'5دقیقه',
                    topic:'دسته بندی',
                    context:'محتوای پست',
                    hasCover:false,
                    cover:'',
                    likes:0
                },
                {
                    title:'موضوع1',
                    authorImageSrc:'',
                    authorName:'1نویسنده',
                    date:'تاریخ1',
                    timeToRead:'5دقیقه',
                    topic:'دسته بندی',
                    context:'محتوای پست',
                    hasCover:true,
                    cover:'',
                    likes:10,
                },
            ]
        }
    },
    methods: {}
}
</script>

<style lang="scss" scoped>
.posts-container{
    width: 650px;
    display: flex;
    flex-direction: column;
    gap: 24px;
}
</style>