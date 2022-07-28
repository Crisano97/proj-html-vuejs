<template>
  <main>
        <WelcomeSection />

        <DoctorsSection />

        <ServicesSection />

        <FacilitiesSection />

        <div class="health-features">
            <MoreInfo v-for="item in moreInfoElements" :key="item.id"
            :item="item"
            />
        </div>

        <AppointmentSection />

        <Carousel />
  </main>
</template>

<script>
import WelcomeSection from './mainComponents/sections/WelcomeSection.vue';
import DoctorsSection from './mainComponents/sections/DoctorsSection.vue';
import ServicesSection from './mainComponents/sections/ServicesSection.vue';
import FacilitiesSection from './mainComponents/sections/FacilitiesSection.vue';
import AppointmentSection from './mainComponents/sections/AppointmentSection.vue';
import MoreInfo from './mainComponents/MoreInfo.vue';
import Carousel from './mainComponents/Carousel.vue';

export default {
    components:{
        WelcomeSection,
        DoctorsSection,
        ServicesSection,
        FacilitiesSection,
        AppointmentSection,
        MoreInfo,
        Carousel,
    },
    data:function(){
        return{
            index: 0,
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
    },
}
</script>

<style lang="scss" >

    @import "../styles/general.scss";

    main{
        color: $secondaryTextColor;
    }

    section{
        padding: 6rem 0;

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

    .c-white{
        color:white;
        hr{
            color: white;
        }
    }

</style>