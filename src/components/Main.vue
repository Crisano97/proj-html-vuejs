<template>
  <main>
    <section class="welcome">
        <div class="container">
            <div class="text-container">
                <h1>Welcome to Avada Health</h1>
                <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Suscipit, quo. Quidem nisi, minus labore laborum facere impedit, quibusdam molestiae cupiditate architecto autem voluptatum! Eius eveniet placeat quos earum fuga vel.</p>
            </div>    
            <div class="features">
                <MainFeatureElement v-for="(feature, index) in welcomeSectionFeatures" :key="index"
                :feature="feature"
                />
            </div>
        </div>
    </section>

    <DoctorsSection />

    <ServicesSection />
    
    <FacilitiesSection />

    <div class="health-features">
        <MoreInfo v-for="item in moreInfoElements" :key="item.id"
        :item="item" 
        />
    </div>

    <AppointmentSection />
    
    <div class="carrasel-container">
      <div class="container">
        
      </div>
    </div>
  </main>
</template>

<script>
import MainFeatureElement from './mainComponents/MainFeatureElement.vue';
import DoctorsSection from './mainComponents/DoctorsSection.vue';
import ServicesSection from './mainComponents/ServicesSection.vue';
import FacilitiesSection from './mainComponents/FacilitiesSection.vue';
import AppointmentSection from './mainComponents/AppointmentSection.vue';
import SectionHead from './mainComponents/SectionHead.vue';
import MoreInfo from './mainComponents/MoreInfo.vue'


export default {
    components:{
        MainFeatureElement,
        DoctorsSection,
        ServicesSection,
        FacilitiesSection,
        AppointmentSection,
        SectionHead,
        MoreInfo,
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
            moreInfoElements: [
                {
                    id: 0,
                    title: 'Emergency Care',
                    imgUrl: '/images/wave-divider.png',
                    text: 'Sed ut perspiciatis unde pmnis iste natus error sit voluptatem accusantium doloremque laudantium, totam rem aperiam, eaque ipsia quae av ill inventore veritatis et quasi architecto beatae',
                },
                {
                    id: 1,
                    title: 'Expert Diagnostics',
                    imgUrl: '/images/wave-divider.png',
                    text: 'Sed ut perspiciatis unde pmnis iste natus error sit voluptatem accusantium doloremque laudantium, totam rem aperiam, eaque ipsia quae av ill inventore veritatis et quasi architecto beatae',
                },
                {
                    id: 2,
                    title: 'Superb Rehabilitation',
                    imgUrl: '/images/wave-divider.png',
                    text: 'Sed ut perspiciatis unde pmnis iste natus error sit voluptatem accusantium doloremque laudantium, totam rem aperiam, eaque ipsia quae av ill inventore veritatis et quasi architecto beatae',
                },
            ],
            
        }
    }
}
</script>

<style lang="scss" >

    @import "../styles/general.scss";

    section{
        padding: 4rem 0;

        div.text-container{
            width: 70%;
            margin: 0 auto;
            font-weight: 100;

            h1{
                font-weight: 100;
            }
            p{
                margin-top: 1.5rem;
            }
            }

        div.features{
            margin-top: 4rem;
            display: flex;
            justify-content: space-between;
            flex-wrap: wrap;
        }
        
    }

    div.container{
            width: 52%;
            margin: 0 auto;
            text-align: center;
            color: $secondaryTextColor;
            line-height: 2rem;
    }
    
    div.health-features{
        width: 100%;
        display: flex;
        justify-content: space-around;
    }

    div.carrasel-container{
        height: 15rem;
        background-image: url('../assets/images/rgb-gradient-bar-for-logo-carrasel.jpg');

    }

    .c-white{
        color:white;
        hr{
            color: white;
        }
    }
</style>