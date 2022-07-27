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
    <section class="doctors">
        <div class="container">
            <SectionType 
            :data="doctorSectionHead"
            />
            <div class="cards-container">
                <DoctorCard v-for="(doctor, index) in doctorsCardsElements" :key="index"
                :doctor="doctor"
                />
            </div>
        </div>
    </section>
    <section class="services">
        <div class="container">
            <SectionType 
            :data="servicesSectionHead"
            />
            <div class="features">
                <MainFeatureElement v-for="(service, index) in servicesSectionElements" :key="index"
                :service="service"
                />
            </div>
        </div>
    </section>
    <section class="facilities">
        <div class="container">
            <SectionType 
            :data="facilitiesSectionHead"
            />
            <img src="../assets/images/play-icon.png" alt="">
        </div>
    </section>
    <div class="health-features">
        <MoreInfo v-for="item in moreInfoElements" :key="item.id"
        :item="item" 
        />
    </div>
    <section class="appointment">
        <div class="container">
            <SectionType 
            :data="appointmentSectionHead"
            />
            <div class="form-container">
                <input type="text" placeholder="Name">
                <input type="text" placeholder="Email">
                <input type="text" placeholder="Phone Number">
                <input type="date">
                <textarea name="" id="" cols="100" rows="10" placeholder="How can we help?"></textarea>
                <button>make an appointment</button>
            </div>
        </div>
    </section>
    <div class="carrasel-container">
      <div class="container">
        
      </div>
    </div>
  </main>
</template>

<script>
import MainFeatureElement from './MainFeatureElement.vue';
import DoctorCard from './DoctorCard.vue';
import SectionType from './SectionType.vue';
import MoreInfo from './MoreInfo.vue'


export default {
    components:{
        MainFeatureElement,
        DoctorCard,
        SectionType,
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
            doctorSectionHead: {
                imgUrl: '/images/icon-5.png',
                title: 'meet our doctors',
                text: 'Sed ut perspiciatis unde pmnis iste natus error sit voluptatem accusantium doloremque laudantium, totam rem aperiam, eaque ipsia quae av ill inventore veritatis et quasi architecto beatae',
            },
            servicesSectionHead: {
                imgUrl: '/images/icon-6.png',
                title: 'our health services',
                text: 'Sed ut perspiciatis unde pmnis iste natus error sit voluptatem accusantium doloremque laudantium, totam rem aperiam, eaque ipsia quae av ill inventore veritatis et quasi architecto beatae',
            },
            facilitiesSectionHead: {
                imgUrl: '/images/icon-7.png',
                title: 'tour our facilities',
                text: 'Sed ut perspiciatis unde pmnis iste natus error sit voluptatem accusantium doloremque laudantium, totam rem aperiam, eaque ipsia quae av ill inventore veritatis et quasi architecto beatae',
            },
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
            appointmentSectionHead: {
                imgUrl: null,
                title: 'Make an appointment',
                text: 'Sed ut perspiciatis unde pmnis iste natus error sit voluptatem accusantium doloremque laudantium, totam rem aperiam, eaque ipsia quae av ill inventore veritatis et quasi architecto beatae',
            },
        }
    }
}
</script>

<style lang="scss" scoped>

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

    section.doctors{
        background-color: $grayBgColor;

        div.cards-container{
            display: flex;
            justify-content: space-between;
        }
    }
    
    section.facilities{
        height: 80vh;
        background-image: url('../assets/images/paralax-bg-tour-facilities.jpg');
        background-size: cover;
        background-position: center;

        img{
            width: 3rem;
            margin-top: 2rem;
            cursor: pointer;
        }
    }

    div.health-features{
        width: 100%;
        display: flex;
        justify-content: space-around;
    }

    section.appointment{
        background-image: url(../assets/images/make-an-appointment.jpg);
        background-size: cover;

        .form-container{
            display: flex;
            justify-content: space-between;
            flex-wrap: wrap;
            gap: 1.5rem;
            margin-top: 2rem;
            
            input{
                width: calc(100% / 2 - 1rem);
                padding: 1rem;
                border: 1px solid white;
                background-color: transparent;
                color: white;
            }

            textarea{
                width: 100%;
                padding: 1rem;
                border: 1px solid white;
                background-color: transparent;
                color: white;
            }

            button{
                background-color: $primaryColorLight;
                border: none;
                width: 100%;
                padding: 1rem 0;
                color: white;
                text-transform: uppercase;
                font-size: 1.2rem;
                cursor: pointer;
            }
        }

    }

    div.carrasel-container{
        height: 15rem;
        background-image: url('../assets/images/rgb-gradient-bar-for-logo-carrasel.jpg');

    }
</style>