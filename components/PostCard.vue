<template>
    <div class="post-card py-4 px-5 ">
        <div class="post-card-header mb-4">
            <div class="author">
                 <div class="author-profile ml-4">
                    <NuxtLink to="/author" >
                        <img :src="post.authorImageSrc ? post.authorImageSrc : 'https://files.virgool.io/upload/users/17855/avatar/qFviiB.png?x-img=v1/resize,h_120,w_120/optimize,q_100'" />
                    </NuxtLink>
                </div>
                <div class="author-info">
                    <NuxtLink to="/author" >{{post.authorName}}</NuxtLink>
                    <p>{{post.date}} - {{post.timeToRead}}</p>
                </div>
            </div>
            <NuxtLink to="/topic" class="topic">{{post.topic}}</NuxtLink>
        </div>
        <div class="post-card-content mb-4">
            <NuxtLink to="/post" >
                <h2 class="mb-4">{{post.title}}</h2>
                <div class="context">
                    <div v-if="post.hasCover" class="cover mb-4">
                        <img :src="post.cover ? post.cover : 'https://cdn.vuetifyjs.com/images/cards/docks.jpg'" alt="">
                    </div>
                    <p>{{post.context}}</p>
                </div>
            </NuxtLink>
        </div>
        <div class="post-card-footer">
            <div class="btn-container">
                <base-button icon :ripple=false text buttonClass='gray-btn like-btn'>
                    <v-icon >
                        mdi-heart-outline 
                    </v-icon>
                </base-button>
                <NuxtLink to="/likes" class="likes mr-2">{{post.likes}}</NuxtLink>
            </div>
            <div class="btn-container">
                <base-button icon :ripple=false text buttonClass='gray-btn'>
                    <v-icon >
                        mdi-bookmark-outline 
                    </v-icon>
                </base-button>
            </div>
        </div>
    </div>
</template>

<script>
import BaseButton from './BaseButton.vue'
export default {
  components: { BaseButton },
    props:{
        post:{
            type:Object
        }
    }
}
</script>

<style lang="scss" scoped>
.post-card{
    background: $white;
    border-radius: 4px;
    box-shadow: 0 0 14px 0 rgba(0 ,0 ,0 , 0.03);

    &-header{
        display: flex;
        justify-content: space-between;

        .author{
            display: flex;
            align-items: center;

            &-profile{
                height: 40px;
                width: 40px;
                
                img{
                    border-radius: 100%;
                    height: 100%;
                    object-fit: cover;
                    width: 100%;
                }
            }

            &-info{
                color: $gray-700;
                font-size: 12.5px;

                a{
                    &:hover{
                        color: $gray-900;
                    }
                }

                p{
                    font-size: 11px;
                    margin-bottom: 0;
                }
            }
        }

        .topic{
            color: $gray-700;
            font-size: 11.2px;
            font-weight: 700;
            height: max-content;

            &:hover{
                color: $gray-900;
            }
        }
    }

    &-content{
        h2{
            color: $gray-900;
            font-size: 20.8px;
            font-weight: 700;
        }

        .context{

            .cover{
                height: 200px;
                overflow: hidden;

                img{
                    height: 100%;
                    -o-object-fit: cover;
                    object-fit: cover;
                    width: 100%;
                }
            }
            

            p{
                color: $gray-600;
                font-size: 14.4px;
                line-height: 1.8;
                margin-bottom:0;
            }
        }
    }

    &-footer{
        display: flex;
        flex-direction: row;
        justify-content: space-between;
        font-size: 14.4px;
        color: $gray-600;
        
        .btn-container{
            display: flex;
            align-items: center;

            .likes{
                font-size: 11.5px;
                color: $gray-700;
            }

        }

    }
}
</style>

