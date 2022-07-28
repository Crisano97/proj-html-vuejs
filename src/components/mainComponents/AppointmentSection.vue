<template>
  <section class="appointment">
        <div class="container">
            <SectionHead class="c-white"
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
</template>

<script>
import SectionHead from './SectionHead.vue';
export default {
    components:{
        SectionHead,
    },
    data:function(){
        return{
            appointmentSectionHead: {
                title: 'Make an Appointment',
                text: 'Sed ut perspiciatis unde pmnis iste natus error sit voluptatem accusantium doloremque laudantium, totam rem aperiam, eaque ipsia quae av ill inventore veritatis et quasi architecto beatae',
            },
        }
    }
}
</script>

<style lang="scss">

    @import "../../styles/general.scss";


    section.appointment{
        background-image: url('../../assets/images/make-an-appointment.jpg');
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
                outline: none;
            }

            textarea{
                width: 100%;
                padding: 1rem;
                border: 1px solid white;
                background-color: transparent;
                color: white;
                outline: none;
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
</style>