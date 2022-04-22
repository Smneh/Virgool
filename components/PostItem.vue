<template>
    <v-card class="post-item">
        <NuxtLink to="/register" class="bg-image-container"> 
            <img 
                class="bg-image"
                :src="post.bgImageSrc ? post.bgImageSrc : 'https://cdn.vuetifyjs.com/images/cards/docks.jpg'"/>
        </NuxtLink>
        <div class="post-caption pa-8">
            <NuxtLink to="/post"><h3>{{post.title}}</h3></NuxtLink>
            <div class="author">
                <div class="author-profile ml-2">
                    <NuxtLink to="/author" >
                        <img :src="post.authorImageSrc ? post.authorImageSrc : 'https://files.virgool.io/upload/users/17855/avatar/qFviiB.png?x-img=v1/resize,h_120,w_120/optimize,q_100'" />
                    </NuxtLink>
                </div>
                <div class="author-info">
                    <NuxtLink to="/author" >{{post.authorName}}</NuxtLink>
                    <time> {{post.date}} </time>
                </div>
            </div>
        </div>
    </v-card>
</template>

<script>
export default {
    props:{
        post:{
            type:Object
        }
    }
}
</script>

<style lang="scss" scoped>
.post-item {
    display: flex;
    flex-direction: column;
    flex: 0 0 auto;
    height: 300px;
    border-radius: 4px;
    overflow: hidden;
    position: relative;
    z-index: 1;
    margin-bottom: 16px;

    a{
        color: inherit;
        text-decoration: none;
    }

    .bg-image-container{
        &::before{
            position: absolute;
            background-color: rgba(0,0,0,.3);
            content: "";
            height: 100%;
            left: 0;
            top: 0;
            width: 100%;
        }

        .bg-image{
            width: 100%;
            height: 100%;
            position: absolute;
            z-index: -1;
        }
    }

    .post-caption{
        bottom: 0;
        position: absolute;
        color: $white;
    
        .author{
            display: flex;
            align-items: center;

            &-profile{
                border-radius: 50%;
                display: inline-block;
                height: 45px;
                width: 45px;
                overflow: hidden;
                vertical-align: middle;

                img{
                    height: 100%;
                    width: 100%;
                    object-fit: cover;
                }
            }

            &-info{
                display: flex;
                flex-direction: column;
                font-size: 12.8px;
            }
        }
    }
}

</style>