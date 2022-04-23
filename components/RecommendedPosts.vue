<template>
    <div class="content-container">
        <div class="section-header mb-4">
            <div class="section-subtitle pt-4">مطالب انتخابی برای شما</div>
        </div>
        <div class="section-body recommended-posts">
            <post-item v-for="(post,index) in posts" :key="index" :post="post" :style="postStyle(index+1)" />
        </div>
    </div>
</template>

<script>
export default {
    data(){
        return{
            posts :[
                {
                    title:'موضوع1',
                    bgImageSrc:'',
                    authorImageSrc:'',
                    authorName:'1نویسنده',
                    date:'تاریخ1'
                },
                {
                    title:'موضوع2',
                    bgImageSrc:'',
                    authorImageSrc:'',
                    authorName:'2نویسنده',
                    date:'تاریخ2'
                },
                {
                    title:'موضوع3',
                    bgImageSrc:'',
                    authorImageSrc:'',
                    authorName:'3نویسنده',
                    date:'تاریخ3'
                },
                {
                    title:'موضوع4',
                    bgImageSrc:'',
                    authorImageSrc:'',
                    authorName:'4نویسنده',
                    date:'تاریخ4'
                },
            ]
        }
    },
    methods: {
        postStyle (index) {
            let style = ''
            if(index === 1 || index === 3)
                style = 'margin-left:16px;'
            return 'grid-area: post-' + index + ';' + style
        }
    }
}
</script>

<style lang="scss" scoped>
.recommended-posts{
    display: grid;
    margin-bottom: 16px;
    grid-template-columns: repeat(8,121px);
    grid-template-rows: repeat(2,auto);
    grid-template-areas: 'post-1 post-1 post-1 post-1 post-1 post-2 post-2 post-2' 
                         'post-3 post-3 post-3 post-4 post-4 post-4 post-4 post-4';
}
</style>