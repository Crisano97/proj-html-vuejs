<template>
  <section class="welcome">
        <div class="container">
            <div class="text-container">
                <h1>
                    Welcome to Avada Health
                </h1>
                <p>
                    Lorem ipsum dolor sit amet consectetur adipisicing elit. Suscipit, quo. Quidem nisi, minus labore laborum facere impedit, quibusdam molestiae cupiditate.
                </p>
            </div>    
            <div class="features">
                <MainFeatureElement v-for="(feature, index) in welcomeSectionFeatures" :key="index"
                :feature="feature"
                />
            </div>
        </div>
    </section>
</template>

<script>

import MainFeatureElement from '../../mainComponents/MainFeatureElement.vue'

export default {
    components:{
        MainFeatureElement,
    },
    data:function(){
        return{
            welcomeSectionFeatures: [
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

<style lang="scss">

    div.text-container{
        width: 70%;
        margin: 0 auto;
        font-weight: 100;
        h1{
            font-weight: 300;
            font-size: 2rem;
        }
        p{
            margin-top: 1.5rem;
            font-weight: 400;
        }
    }
</style>