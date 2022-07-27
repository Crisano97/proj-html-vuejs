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
    
    <div class="carrasel-container">
      <div class="container">
        
      </div>
    </div>
  </main>
</template>

<script>
import WelcomeSection from './mainComponents/WelcomeSection.vue';
import DoctorsSection from './mainComponents/DoctorsSection.vue';
import ServicesSection from './mainComponents/ServicesSection.vue';
import FacilitiesSection from './mainComponents/FacilitiesSection.vue';
import AppointmentSection from './mainComponents/AppointmentSection.vue';
import MoreInfo from './mainComponents/MoreInfo.vue'


export default {
    components:{
        WelcomeSection,
        DoctorsSection,
        ServicesSection,
        FacilitiesSection,
        AppointmentSection,
        MoreInfo,
    },
    data:function(){
        return{
                          
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