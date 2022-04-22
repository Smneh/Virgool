<template>
     <div class="content-container py-8 mb-8">
       <div class="promotion-box">
           <div class="promotion-context pa-8">
                <h3 class="pt-4 pb-6 ma-0">به ویرگول، دنیای کلمات خوش آمدید.<i>👋</i></h3>
                <p class="mb-3">
                ویرگول بستری برای خواندن، گفتگو درباره‌ی موضوعات مورد علاقه و به اشتراک‌گذاری ایده‌های اصیل و عمیق در زندگی شخصی، حرفه‌ای و اجتماعی است.
                </p>
                <div class="buttons-container pt-4">
                    <base-button outlined buttonClass="py-2 px-4" to='/'>اطلاعات بیشتر</base-button>
                    <base-button text buttonClass='primary-btn start-btn py-2 px-4' :ripple=false to=/ >شروع به کار</base-button>
                </div>
           </div>
        </div>
    </div>
</template>

<script>
import BaseButton from './BaseButton.vue'
    export default {
  components: { BaseButton },
        
    }
</script>

<style lang="scss" scoped>
.promotion-box{
    display: flex;
    width: 100%;
    height: 300px;
    overflow: hidden;
    background-color: $light-pale-blue;
    background-image: url(../assets/typewriter.png);
    background-repeat: no-repeat;
    background-size: 318px;

    .promotion-context{
        display: flex;
        flex-direction: column;
        font-weight: 600;
        width: 55%;

        h3{
            font-size: 22px;
            font-weight: 500;
        }

        p{
            color: $light-gray;
            font-size: 13.5px;
        }

        .buttons-container{
            display: flex;
            gap: 8px;
        }
    }
}
</style>