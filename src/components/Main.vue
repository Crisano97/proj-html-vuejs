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
            <!-- <SectionType /> -->
            <div class="section-type">
                <img src="../assets/images/icon-5.png" alt="doctor icon">
                <h2>meet our doctors</h2>
                <hr>
                <span>
                    Sed ut perspiciatis unde pmnis iste natus error sit voluptatem accusantium doloremque laudantium, totam rem aperiam, eaque ipsia quae av ill inventore veritatis et quasi architecto beatae
                </span>
            </div>
            <div class="cards-container">
                <DoctorCard v-for="(doctor, index) in doctorsCardsElements" :key="index"
                :doctor="doctor"
                />
            </div>
        </div>
    </section>
  </main>
</template>

<script>
import MainFeatureElement from './MainFeatureElement.vue';
import DoctorCard from './DoctorCard.vue';
// import SectionType from './SectionType.vue';


export default {
    components:{
        MainFeatureElement,
        DoctorCard,
        // SectionType,
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
            ]
            // section: [
            //     {
            //         imgUrl: './images/icon.5.png',
            //         title: 'meet our doctors',
            //         text: 'Sed ut perspiciatis unde pmnis iste natus error sit voluptatem accusantium doloremque laudantium, totam rem aperiam, eaque ipsia quae av ill inventore veritatis et quasi architecto beatae',
            //     }
            // ]
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
            }
        }
    }

    section.doctors{
        background-color: $grayBgColor;

        div.section-type{
            width: 70%;
            margin: 0 auto;

            h2{
                font-size: 2rem;
                text-transform: uppercase;
                font-weight: 100;
            }

            hr{
                width: 40%;
                margin: 2rem auto;
                opacity: .3;
            }
        }

        div.cards-container{
            display: flex;
            justify-content: space-between;
        }
    }
    
</style>