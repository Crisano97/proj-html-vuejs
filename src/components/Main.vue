<template>
  <main>
    <section class="welcome">
        <div class="container">
            <div class="text-container">
                <h1>Welcome to Avada Health</h1>
                <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Suscipit, quo. Quidem nisi, minus labore laborum facere impedit, quibusdam molestiae cupiditate architecto autem voluptatum! Eius eveniet placeat quos earum fuga vel.</p>
            </div>    
            <div class="features">
                <MainFeatureElement v-for="(feature, index) in welcomeSectionFeature" :key="index"
                :feature="feature"
                />
            </div>
        </div>
    </section>
  </main>
</template>

<script>
import MainFeatureElement from './MainFeatureElement.vue';

export default {
    components:{
        MainFeatureElement,
    },
    data:function(){
        return{
            welcomeSectionFeature: [
                {
                    imgUrl: '/images/icon-1.png',
                    title: 'same day appointments',
                    text: 'Sed ut perispiciatis unde omnie isste natys error sit voluptam accusantim.'
                },
                {
                    imgUrl: '/images/icon-2.png',
                    title: 'world class facilities',
                    text: 'Sed ut perispiciatis unde omnie isste natys error sit voluptam accusantim.'
                },
                {
                    imgUrl: '/images/icon-3.png',
                    title: 'expert doctors',
                    text: 'Sed ut perispiciatis unde omnie isste natys error sit voluptam accusantim.'
                },
                {
                    imgUrl: '/images/icon-4.png',
                    title: 'complementary therapies',
                    text: 'Sed ut perispiciatis unde omnie isste natys error sit voluptam accusantim.'
                },
            ],
        }
    }
}
</script>

<style lang="scss" scoped>

    @import "../styles/general.scss";

    section{
        padding: 4rem 0;
        div.container{
            width: 52%;
            margin: 0 auto;
            text-align: center;
            color: $secondaryTextColor;
            line-height: 2rem;

            div.text-container{
                width: 60%;
                margin: 0 auto;

                p{
                    margin-top: 1.5rem;
                }
            }

            div.features{
                margin-top: 4rem;
                display: flex;
                justify-content: space-between;
            }
        }

    }
    
</style>