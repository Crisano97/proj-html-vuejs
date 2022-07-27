<template>
  <section class="services">
        <div class="container">
            <SectionHead 
            :data="servicesSectionHead"
            />
            <div class="features">
                <MainFeatureElement v-for="(service, index) in servicesSectionElements" :key="index"
                :service="service"
                />
            </div>
        </div>
    </section>
</template>

<script>

import SectionHead from './SectionHead.vue';
import MainFeatureElement from './MainFeatureElement.vue';


export default {
    components:{
        SectionHead,
        MainFeatureElement,
    },
    data:function(){
        return{
            servicesSectionHead: {
                imgUrl: '/images/icon-6.png',
                title: 'our health services',
                text: 'Sed ut perspiciatis unde pmnis iste natus error sit voluptatem accusantium doloremque laudantium, totam rem aperiam, eaque ipsia quae av ill inventore veritatis et quasi architecto beatae',
            },
            servicesSectionElements:[
                {
                    imgUrl: '/images/icon-14.png',
                    title: 'reambulation center',
                    text: 'Sed ut perispiciatis unde omnie isste natys error sit voluptam accusantim.'
                },
                {
                    imgUrl: '/images/icon-15.png',
                    title: 'dental implants',
                    text: 'Sed ut perispiciatis unde omnie isste natys error sit voluptam accusantim.'
                },
                {
                    imgUrl: '/images/icon-16.png',
                    title: 'medicine researc',
                    text: 'Sed ut perispiciatis unde omnie isste natys error sit voluptam accusantim.'
                },
                {
                    imgUrl: '/images/icon-11.png',
                    title: 'blood bank',
                    text: 'Sed ut perispiciatis unde omnie isste natys error sit voluptam accusantim.'
                },
                {
                    imgUrl: '/images/icon-12.png',
                    title: 'pharmaceutical advice',
                    text: 'Sed ut perispiciatis unde omnie isste natys error sit voluptam accusantim.'
                },{
                    imgUrl: '/images/icon-13.png',
                    title: 'medical coounseling',
                    text: 'Sed ut perispiciatis unde omnie isste natys error sit voluptam accusantim.'
                },
            ],
        }
    }
}
</script>

<style>

</style>