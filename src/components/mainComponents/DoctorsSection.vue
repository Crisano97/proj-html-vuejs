<template>
  <section class="doctors">
        <div class="container">
            <SectionHead 
            :data="doctorSectionHead"
            />
            <div class="cards-container">
                <DoctorCard v-for="(doctor, index) in doctorsCardsElements" :key="index"
                    :doctor="doctor"
                />
            </div>
            
        </div>
    </section>
</template>

<script>

import SectionHead from './SectionHead.vue';
import DoctorCard from './DoctorCard.vue';


export default {
    components:{
        SectionHead,
        DoctorCard,
    },
    data:function(){
        return{
            doctorSectionHead: {
                imgUrl: '/images/icon-5.png',
                title: 'meet our doctors',
                text: 'Sed ut perspiciatis unde pmnis iste natus error sit voluptatem accusantium doloremque laudantium, totam rem aperiam, eaque ipsia quae av ill inventore veritatis et quasi architecto beatae',
            },
            doctorsCardsElements: [
                {
                    imgUrl:'/images/doctor-1.jpg',
                    name: 'jown snow',
                    role: 'Anasthesiologist',
                    description: 'Lorem ipsum dolor sit, amet consectetur adipisicing elit. A ad itaque officiis voluptatem iusto.',
                },
                {
                    imgUrl:'/images/doctor-2.jpg',
                    name: 'tony stark',
                    role: 'Cardiologist',
                    description: 'Lorem ipsum dolor sit, amet consectetur adipisicing elit. A ad itaque officiis voluptatem iusto.',
                },
                {
                    imgUrl:'/images/doctor-3.jpg',
                    name: 'anna smith',
                    role: 'Nurse Practitioner',
                    description: 'Lorem ipsum dolor sit, amet consectetur adipisicing elit. A ad itaque officiis voluptatem iusto.',
                },
            ],
        }
    }
}
</script>

<style lang="scss">

    @import "../../styles/general.scss"; 

    section.doctors{
        background-color: $grayBgColor;

        div.cards-container{
            display: flex;
            justify-content: space-between;
        }
    }

</style>